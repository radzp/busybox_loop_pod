# busybox_loop_pod

# Kubernetes Lab: Pod Wykonujący Zadanie (BusyBox Loop)

Proces polegał na utworzeniu poda w Kubernetes, który ma za zadanie wykonać jednorazowy skrypt w kontenerze **BusyBox**, oraz proces modyfikacji Poda w celu utrzymania stanu `Running`. 

Wygenerowanie bazowego manifestu YAML i jego edycji, aby zawierał pętlę i poprawną politykę restartu dla zadań jednorazowych.

Użycie `dry-run` do szybkiego wygenerowania szablonu:

```bash
kubectl run loop --image=busybox:1.36.1 --restart=Never --dry-run=client -o yaml -- sleep 1000 > loop-pod.yaml
```


### Zawartość pliku loop-pod.yaml
<img width="828" height="511" alt="Zrzut ekranu 2025-11-3 o 11 56 35 PM" src="https://github.com/user-attachments/assets/6f9b271a-0b98-4bc3-a6e3-077bc211b3c0" />

### Status poda po uruchomieniu 

<img width="832" height="367" alt="Zrzut ekranu 2025-11-3 o 11 58 48 PM" src="https://github.com/user-attachments/assets/3f23c0c5-f1ee-4bb7-83b7-1d781d741b2e" />

### Modyfikacja pliku yaml - dodanie pętli nieskończonej

<img width="823" height="499" alt="Zrzut ekranu 2025-11-3 o 11 59 49 PM" src="https://github.com/user-attachments/assets/c0c27920-d114-439b-bbe7-71799f996d28" />

### Wynik działania po uruchomieniu:

<img width="829" height="424" alt="Zrzut ekranu 2025-11-4 o 12 00 18 AM" src="https://github.com/user-attachments/assets/406052ec-3daa-4a44-90fc-cdb7a4f9accf" />



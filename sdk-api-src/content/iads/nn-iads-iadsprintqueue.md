---
UID: NN:iads.IADsPrintQueue
title: IADsPrintQueue (iads.h)
description: The IADsPrintQueue interface represents a printer on a network.
helpviewer_keywords: ["IADsPrintQueue","IADsPrintQueue interface [ADSI]","IADsPrintQueue interface [ADSI]","described","_ds_iadsprintqueue","adsi.iadsprintqueue","iads/IADsPrintQueue"]
old-location: adsi\iadsprintqueue.htm
tech.root: adsi
ms.assetid: 2ea956b0-fb8f-4ffb-8741-8d98ad05d783
ms.date: 12/05/2018
ms.keywords: IADsPrintQueue, IADsPrintQueue interface [ADSI], IADsPrintQueue interface [ADSI],described, _ds_iadsprintqueue, adsi.iadsprintqueue, iads/IADsPrintQueue
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsPrintQueue
 - iads/IADsPrintQueue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsPrintQueue
---

# IADsPrintQueue interface


## -description

The <b>IADsPrintQueue</b> interface represents a printer on a network. It is a dual interface that inherits from <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. The property methods of this interface enables you to access data about a printer, for example printer model, physical location, and network address.

## -inheritance

The <b>IADsPrintQueue</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsPrintQueue</b> also has these types of members:

## -remarks

Use this interface to browse a collection of print jobs in the print queue. To control a printer across a network, use the  <a href="/windows/desktop/api/iads/nn-iads-iadsprintqueueoperations">IADsPrintQueueOperations</a> interface. To obtain a collection of the print jobs, call the  <a href="/windows/desktop/api/iads/nf-iads-iadsprintqueueoperations-printjobs">IADsPrintQueueOperations::PrintJobs</a> method.

In Windows, a printer, or a print queue, is managed by a host computer. If the path to a print queue is known, bind to it as to any other ADSI objects.

The following Visual Basic code example shows the bind operation.


```vb
Dim pq as IADsPrintQueue
Set pq = GetObject("WinNT://aMachine/aPrinter")
```


The following C++ code example shows the bind operation.


```cpp
IADsPrintQueue *pq;
LPWSTR adsPath = L"WinNT://aMachine/aPrinter";
HRESULT hr = ADsGetObject(adsPath,
                          IID_IADsPrintQueue,
                          (void**)&pq);
```


<p class="proch"><b>To enumerate all print queues on a given computer</b>

<ol>
<li>Bind to the computer object.</li>
<li>Determine if the computer contains any "PrintQueue" objects.</li>
<li>Enumerate all the found printer objects.</li>
</ol>

#### Examples

The following code example enumerates printers on a given computer.


```vb
Dim cont As IADsContainer
Dim pq As IADsPrintQueue

On Error GoTo Cleanup
 
' Bind to the computer object
Set cont = GetObject("WinNT://fabrikam1,computer")

cont.Filter = Array("PrintQueue")

For Each p In cont
   Set pq = GetObject(p.ADsPath)
   MsgBox pq.Name & " is a " & pq.Model
Next p

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set pq = Nothing
```

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/ADSI/iadsprintqueue-property-methods">IADsPrintQueue Property Methods</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsprintqueueoperations">IADsPrintQueueOperations</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsprintqueueoperations-printjobs">IADsPrintQueueOperations::PrintJobs</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>

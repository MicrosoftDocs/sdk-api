---
UID: NN:iads.IADsPrintJob
title: IADsPrintJob (iads.h)
description: The IADsPrintJob interface is a dual interface that inherits from IADs.
helpviewer_keywords: ["IADsPrintJob","IADsPrintJob interface [ADSI]","IADsPrintJob interface [ADSI]","described","_ds_iadsprintjob","adsi.iadsprintjob","iads/IADsPrintJob"]
old-location: adsi\iadsprintjob.htm
tech.root: adsi
ms.assetid: 82d61e39-4dbb-41c9-85d5-6f4e7ab7f66b
ms.date: 12/05/2018
ms.keywords: IADsPrintJob, IADsPrintJob interface [ADSI], IADsPrintJob interface [ADSI],described, _ds_iadsprintjob, adsi.iadsprintjob, iads/IADsPrintJob
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
 - IADsPrintJob
 - iads/IADsPrintJob
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
 - IADsPrintJob
---

# IADsPrintJob interface


## -description

The <b>IADsPrintJob</b> interface is a dual interface that inherits from <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is designed for representing a print job. When a user submits a request to a printer to print a document, a print job is created in the print queue. The property methods allow you to access the information about a print job. Such information includes which printer performs the printing, who submitted the document, when the document was submitted, and how many pages will be printed.

## -inheritance

The <b>IADsPrintJob</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsPrintJob</b> also has these types of members:

## -remarks

To manage a print job across a network, use the  <a href="/windows/desktop/api/iads/nn-iads-iadsprintjoboperations">IADsPrintJobOperations</a> interface, which supports the functionality to examine the status of a print job and to pause or resume the operation of printing the document, and so on.

To access any print jobs in a print queue, call the  <a href="/windows/desktop/api/iads/nf-iads-iadsprintqueueoperations-printjobs">IADsPrintQueueOperations::PrintJobs</a> method to obtain the collection object holding all the print jobs in the print queue.


#### Examples

The following code example shows how to manage a print job submitted to the printer, "\\aMachine\aPrinter".


```vb
Dim pq As IADsPrintQueue
Dim pqo As IADsPrintQueueOperations
Dim pj As IADsPrintJob
Dim pjo As IADsPrintJobOperations
Dim pjs As IADsCollection

On Error GoTo Cleanup
 
Set pq = GetObject("WinNT://aMachine/aPrinter")
Set pqo = pq
For Each pj In pqo.PrintJobs
   MsgBox pj.class 
   MsgBox pj.description 
   MsgBox pj.HostPrintQueue
   Set pjo = pj
   If Hex(pjo.status) = 10 ' printing
      pjo.Pause
   Else
      pjo.Resume
  End If
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pq = Nothing
    Set pqo = Nothing
    Set pj = Nothing
    Set pjo = Nothing
    Set pjs = Nothing
```


The following code example shows how to manage a print job submitted to the printer, "\\aMachine\aPrinter".


```cpp
IADsPrintJobOperations *pjo = NULL;
IADsPrintQueueOperations *pqo = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
IEnumVARIANT *pEnum = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;

long status;

HRESULT hr = S_OK;
hr = ADsGetObject(L"WinNT://aMachine/aPrinter", 
                  IID_IADsPrintQueueOperations, 
                  (void**)&pqo);
if(FAILED(hr)){goto Cleanup;}

hr = pqo->PrintJobs(&pColl);

hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)){goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)){goto Cleanup;}

// Now Enumerate
VariantInit(&var);
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsPrintJobOperations, 
                              (void**)&pjo);

        pjo->get_Status(&status);
        printf("Job status: %x\n",status);
        if(stats == ADS_JOB_PRINTING) {
            pjo.Pause();
        }
        else {
            pjo.Resume();
        }
        pjo->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    VariantClear(&var);
    if(pColl) pColl->Release();
    if(pUnk) pUnk->Release();
    if(pEnum) pEnum->Release();
    if(pqo) pqo->Release();
```

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/ADSI/iadsprintjob-property-methods">IADsPrintJob Property Methods</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsprintjoboperations">IADsPrintJobOperations</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsprintqueueoperations-printjobs">IADsPrintQueueOperations::PrintJobs</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>

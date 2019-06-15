---
UID: NN:iads.IADsPrintJob
title: IADsPrintJob (iads.h)
author: windows-sdk-content
description: The IADsPrintJob interface is a dual interface that inherits from IADs.
old-location: adsi\iadsprintjob.htm
tech.root: adsi
ms.assetid: 82d61e39-4dbb-41c9-85d5-6f4e7ab7f66b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IADsPrintJob, IADsPrintJob interface [ADSI], IADsPrintJob interface [ADSI],described, _ds_iadsprintjob, adsi.iadsprintjob, iads/IADsPrintJob
ms.topic: interface
f1_keywords: ["iads/IADsPrintJob"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsPrintJob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsPrintJob interface


## -description


The <b>IADsPrintJob</b> interface is a dual interface that inherits from <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is designed for representing a print job. When a user submits a request to a printer to print a document, a print job is created in the print queue. The property methods allow you to access the information about a print job. Such information includes which printer performs the printing, who submitted the document, when the document was submitted, and how many pages will be printed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsPrintJob</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsPrintJob</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsPrintJob</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-get">Get</a>
</td>
<td align="left" width="63%">
Gets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getex">GetEx</a>
</td>
<td align="left" width="63%">
Gets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getinfo">GetInfo</a>
</td>
<td align="left" width="63%">
Loads the property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getinfoex">GetInfoEx</a>
</td>
<td align="left" width="63%">
Loads specific property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-put">Put</a>
</td>
<td align="left" width="63%">
Sets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-putex">PutEx</a>
</td>
<td align="left" width="63%">
Sets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-setinfo">SetInfo</a>
</td>
<td align="left" width="63%">
Persists the changes on this object to the underlying directory store.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsPrintJob</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">AdsPath</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the object's ADsPath that uniquely identifies this object from all others.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">Class</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the name of the object's schema class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintjob-property-methods">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the description of the print job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">GUID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the GUID of the object as stored in the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintjob-property-methods">HostPrintQueue</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the ADsPath string that names the print queue processing this print job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the object's relative name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintjob-property-methods">Notify</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the user to be notified when job is completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintjob-property-methods">NotifyPath</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The ADsPath string for user to be notified when the job is completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">Parent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the ADsPath string for the parent of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintjob-property-methods">Priority</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the priority of the print job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iads-property-methods">Schema</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the ADsPath string to the schema class object for this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintjob-property-methods">Size</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the size, in bytes, of the print job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintjob-property-methods">StartTime</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the earliest time when the print job should be started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintjob-property-methods">TimeSubmitted</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the time when the job was submitted to the print queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintjob-property-methods">TotalPages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the total number of pages in the print job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintjob-property-methods">UntilTime</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the time when the print job should be stopped.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintjob-property-methods">User</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Name of user that submitted the print job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintjob-property-methods">UserPath</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the ADsPath name for user to submit the print job.

</td>
</tr>
</table> 


## -remarks



To manage a print job across a network, use the  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsprintjoboperations">IADsPrintJobOperations</a> interface, which supports the functionality to examine the status of a print job and to pause or resume the operation of printing the document, and so on.

To access any print jobs in a print queue, call the  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsprintqueueoperations-printjobs">IADsPrintQueueOperations::PrintJobs</a> method to obtain the collection object holding all the print jobs in the print queue.


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




<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintjob-property-methods">IADsPrintJob Property Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsprintjoboperations">IADsPrintJobOperations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsprintqueueoperations-printjobs">IADsPrintQueueOperations::PrintJobs</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 


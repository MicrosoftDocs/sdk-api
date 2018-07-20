---
UID: NN:iads.IADsPrintJob
title: IADsPrintJob
author: windows-sdk-content
description: The IADsPrintJob interface is a dual interface that inherits from IADs.
old-location: adsi\iadsprintjob.htm
old-project: ADSI
ms.assetid: 82d61e39-4dbb-41c9-85d5-6f4e7ab7f66b
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IADsPrintJob, IADsPrintJob interface [ADSI], IADsPrintJob interface [ADSI],described, _ds_iadsprintjob, adsi.iadsprintjob, iads/IADsPrintJob
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: ADS_SD_FORMAT_ENUM
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
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsPrintJob interface


## -description


The <b>IADsPrintJob</b> interface is a dual interface that inherits from <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>. It is designed for representing a print job. When a user submits a request to a printer to print a document, a print job is created in the print queue. The property methods allow you to access the information about a print job. Such information includes which printer performs the printing, who submitted the document, when the document was submitted, and how many pages will be printed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsPrintJob</b> interface inherits from <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> and <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>. <b>IADsPrintJob</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>
</td>
<td align="left" width="63%">
Gets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cda6b8e7-fadc-4e0b-8217-66b37bf7efbd">GetEx</a>
</td>
<td align="left" width="63%">
Gets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451309">GetInfo</a>
</td>
<td align="left" width="63%">
Loads the property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/306ab953-890a-4ec9-8ec2-bea73888ea20">GetInfoEx</a>
</td>
<td align="left" width="63%">
Loads specific property values of this object from the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">Put</a>
</td>
<td align="left" width="63%">
Sets the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb9d9b2c-9efc-4462-ac4b-9a2fbf0b5ec7">PutEx</a>
</td>
<td align="left" width="63%">
Sets the value for a single or multi-valued property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">SetInfo</a>
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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">AdsPath</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Class</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>


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

<a href="https://msdn.microsoft.com/23e7cbf3-09ce-44ce-b618-2c0fa6b34428">HostPrintQueue</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


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

<a href="https://msdn.microsoft.com/23e7cbf3-09ce-44ce-b618-2c0fa6b34428">Notify</a>


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

<a href="https://msdn.microsoft.com/23e7cbf3-09ce-44ce-b618-2c0fa6b34428">NotifyPath</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Parent</a>


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

<a href="https://msdn.microsoft.com/23e7cbf3-09ce-44ce-b618-2c0fa6b34428">Priority</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Schema</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">Size</a>


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

<a href="https://msdn.microsoft.com/23e7cbf3-09ce-44ce-b618-2c0fa6b34428">StartTime</a>


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

<a href="https://msdn.microsoft.com/23e7cbf3-09ce-44ce-b618-2c0fa6b34428">TimeSubmitted</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn265411">TotalPages</a>


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

<a href="https://msdn.microsoft.com/23e7cbf3-09ce-44ce-b618-2c0fa6b34428">UntilTime</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/mt270121">User</a>


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

<a href="https://msdn.microsoft.com/23e7cbf3-09ce-44ce-b618-2c0fa6b34428">UserPath</a>


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



To manage a print job across a network, use the  <a href="https://msdn.microsoft.com/259f6c3d-73ec-4110-801a-c83ffca0f830">IADsPrintJobOperations</a> interface, which supports the functionality to examine the status of a print job and to pause or resume the operation of printing the document, and so on.

To access any print jobs in a print queue, call the  <a href="https://msdn.microsoft.com/fe92fef3-596f-416c-b613-1d93737c298e">IADsPrintQueueOperations::PrintJobs</a> method to obtain the collection object holding all the print jobs in the print queue.


#### Examples

The following code example shows how to manage a print job submitted to the printer, "\\aMachine\aPrinter".

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim pq As IADsPrintQueue
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
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set pq = Nothing
    Set pqo = Nothing
    Set pj = Nothing
    Set pjo = Nothing
    Set pjs = Nothing</pre>
</td>
</tr>
</table></span></div>
The following code example shows how to manage a print job submitted to the printer, "\\aMachine\aPrinter".

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADsPrintJobOperations *pjo = NULL;
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
                  (void**)&amp;pqo);
if(FAILED(hr)){goto Cleanup;}

hr = pqo-&gt;PrintJobs(&amp;pColl);

hr = pColl-&gt;get__NewEnum(&amp;pUnk);
if(FAILED(hr)){goto Cleanup;}

hr = pUnk-&gt;QueryInterface(IID_IEnumVARIANT,(void**)&amp;pEnum);
if(FAILED(hr)){goto Cleanup;}

// Now Enumerate
VariantInit(&amp;var);
hr = pEnum-&gt;Next(1, &amp;var, &amp;lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&amp;var);
        pDisp-&gt;QueryInterface(IID_IADsPrintJobOperations, 
                              (void**)&amp;pjo);

        pjo-&gt;get_Status(&amp;status);
        printf("Job status: %x\n",status);
        if(stats == ADS_JOB_PRINTING) {
            pjo.Pause();
        }
        else {
            pjo.Resume();
        }
        pjo-&gt;Release();
    }
    pDisp-&gt;Release();
    VariantClear(&amp;var);
    hr = pEnum-&gt;Next(1, &amp;var, &amp;lFetch);
};

Cleanup:
    VariantClear(&amp;var);
    if(pColl) pColl-&gt;Release();
    if(pUnk) pUnk-&gt;Release();
    if(pEnum) pEnum-&gt;Release();
    if(pqo) pqo-&gt;Release();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/23e7cbf3-09ce-44ce-b618-2c0fa6b34428">IADsPrintJob Property Methods</a>



<a href="https://msdn.microsoft.com/259f6c3d-73ec-4110-801a-c83ffca0f830">IADsPrintJobOperations</a>



<a href="https://msdn.microsoft.com/fe92fef3-596f-416c-b613-1d93737c298e">IADsPrintQueueOperations::PrintJobs</a>



<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 


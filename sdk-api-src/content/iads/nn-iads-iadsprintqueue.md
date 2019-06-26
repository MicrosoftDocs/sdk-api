---
UID: NN:iads.IADsPrintQueue
title: IADsPrintQueue (iads.h)
author: windows-sdk-content
description: The IADsPrintQueue interface represents a printer on a network.
old-location: adsi\iadsprintqueue.htm
tech.root: adsi
ms.assetid: 2ea956b0-fb8f-4ffb-8741-8d98ad05d783
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IADsPrintQueue, IADsPrintQueue interface [ADSI], IADsPrintQueue interface [ADSI],described, _ds_iadsprintqueue, adsi.iadsprintqueue, iads/IADsPrintQueue
ms.topic: interface
f1_keywords: 
 - "iads/IADsPrintQueue"
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
 - IADsPrintQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsPrintQueue interface


## -description


The <b>IADsPrintQueue</b> interface represents a printer on a network. It is a dual interface that inherits from <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>. The property methods of this interface enables you to access data about a printer, for example printer model, physical location, and network address.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsPrintQueue</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsPrintQueue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsPrintQueue</b> interface has these methods.
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
Retrieves the value for a property by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getex">GetEx</a>
</td>
<td align="left" width="63%">
Retrieves the value for a single or multi-valued property by name.

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
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsPrintQueue</b> interface has these properties.
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
Retrieves the object ADsPath that uniquely identifies this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintqueue-property-methods">BannerPage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves and sets the file system path to the banner page file used to separate jobs.

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
Retrieves the name of the object schema class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintqueue-property-methods">Datatype</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves and sets the data type that can be processed by this print queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintqueue-property-methods">DefaultJobPriority</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves and sets the default priority assigned to each print job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintqueue-property-methods">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves and sets the description of this print queue.

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
Retrieves the GUID of the object as stored in the underlying directory store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintqueue-property-methods">Location</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves and sets the administrator description of the print queue location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintqueue-property-methods">Model</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves and sets the name of the driver used by this print queue.

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
Retrieves the object relative name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintqueue-property-methods">NetAddresses</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves and sets the binding data.

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
Retrieves the ADsPath string for the object parent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintqueue-property-methods">PrintDevices</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves and sets the names of print devices that this print queue uses as spooling devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintqueue-property-methods">PrinterPath</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves and sets the path where a shared printer can be accessed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintqueue-property-methods">PrintProcessor</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves and sets the print processor associated with this print queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintqueue-property-methods">Priority</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves and sets the priority of this printer object job queue for connected devices.

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
Retrieves the ADsPath string to the schema class object for this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintqueue-property-methods">StartTime</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves and sets the time when the print queue starts processing jobs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintqueue-property-methods">UntilTime</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves and sets the time at which the print queue stops processing jobs.

</td>
</tr>
</table> 


## -remarks



Use this interface to browse a collection of print jobs in the print queue. To control a printer across a network, use the  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsprintqueueoperations">IADsPrintQueueOperations</a> interface. To obtain a collection of the print jobs, call the  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsprintqueueoperations-printjobs">IADsPrintQueueOperations::PrintJobs</a> method.

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


<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To enumerate all print queues on a given computer</b>

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




<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsprintqueue-property-methods">IADsPrintQueue Property Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsprintqueueoperations">IADsPrintQueueOperations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsprintqueueoperations-printjobs">IADsPrintQueueOperations::PrintJobs</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 


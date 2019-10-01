---
UID: NN:iads.IADsService
title: IADsService (iads.h)
author: windows-sdk-content
description: The IADsService interface is a dual interface that inherits from IADs.
old-location: adsi\iadsservice.htm
tech.root: adsi
ms.assetid: b59a6594-1109-4913-8a83-4888e56e71d0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IADsService, IADsService interface [ADSI], IADsService interface [ADSI],described, _ds_iadsservice, adsi.iadsservice, iads/IADsService
ms.topic: interface
f1_keywords: 
 - "iads/IADsService"
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
 - IADsService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsService interface


## -description


The <b>IADsService</b> interface is a dual interface that inherits from <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is designed to maintain data about system services running on a host computer. Examples of such services include "FAX" for Microsoft Fax Service, "RemoteAccess" for Routing and RemoteAccess Service, and "seclogon" for Secondary Logon Service. Examples of the data about any system service include the path to the executable file on the host computer, the type of the service, other services or load group required to run a particular service, and others. <b>IADsService</b> exposes several properties to represent such data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsService</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsService</b> interface has these methods.
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
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsService</b> interface has these properties.
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

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsservice-property-methods">Dependencies</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the array of <b>BSTR</b> names of services or load groups that must be loaded in order for this service to load.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsservice-property-methods">DisplayName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the display name of this service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsservice-property-methods">ErrorControl</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the actions taken in case of service failure.

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

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsservice-property-methods">HostComputer</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the host of this service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsservice-property-methods">LoadOrderGroup</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the load order group for this service.

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

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsservice-property-methods">Path</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the path and filename of the executable.

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

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsservice-property-methods">ServiceAccountName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the authentication account name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsservice-property-methods">ServiceAccountPath</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the path to user object to authenticate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsservice-property-methods">ServiceType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the process type in which this service runs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsservice-property-methods">StartType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a value that determines how the service is started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsservice-property-methods">StartupParameters</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the parameters passed at start-up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsservice-property-methods">Version</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the version data of this service.

</td>
</tr>
</table> 


## -remarks



The system services are published in the underlying directory. Some may be running, others may not. To verify the status or to operate on any of the services, use the properties and methods of the  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsserviceoperations">IADsServiceOperations</a> interface.

File service is a special case of the system service. The  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsfileservice">IADsFileService</a> and  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations">IADsFileServiceOperations</a> interfaces support additional features unique to file services.


#### Examples

To identify services available on a host computer, first bind to the computer and then enumerate the services available on that computer. The following code example shows  how to do this.


```vb
Public Sub ListServicesOnComputer(ComputerName As String)
    Dim comp As IADsComputer
    Dim srvc As IADsServiceOperations
    
    On Error GoTo Cleanup
    
    Set comp = GetObject("WinNT://" + ComputerName + ",Computer")
    comp.Filter = Array("Service")
    For Each srvc In comp
        ' The srvc object is an IADsServiceOperations object that can be 
        ' used to obtain the status of the service with the Status property. 
        ' Other IADs properties can also be obtained.
    Next
    
Cleanup:
    If (Err.Number <> 0) Then
        MsgBox (Err.Description & vbLf & vbLf & " Error number = " & Err.Number)
    End If
    Set comp = Nothing
End Sub
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsfileservice">IADsFileService</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations">IADsFileServiceOperations</a>



<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsservice-property-methods">IADsService Property Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsserviceoperations">IADsServiceOperations</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 


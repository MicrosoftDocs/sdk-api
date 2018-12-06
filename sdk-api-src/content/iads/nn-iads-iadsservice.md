---
UID: NN:iads.IADsService
title: IADsService
author: windows-sdk-content
description: The IADsService interface is a dual interface that inherits from IADs.
old-location: adsi\iadsservice.htm
tech.root: adsi
ms.assetid: b59a6594-1109-4913-8a83-4888e56e71d0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IADsService, IADsService interface [ADSI], IADsService interface [ADSI],described, _ds_iadsservice, adsi.iadsservice, iads/IADsService
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsService interface


## -description


The <b>IADsService</b> interface is a dual interface that inherits from <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>. It is designed to maintain data about system services running on a host computer. Examples of such services include "FAX" for Microsoft Fax Service, "RemoteAccess" for Routing and RemoteAccess Service, and "seclogon" for Secondary Logon Service. Examples of the data about any system service include the path to the executable file on the host computer, the type of the service, other services or load group required to run a particular service, and others. <b>IADsService</b> exposes several properties to represent such data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsService</b> interface inherits from <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> and <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>. <b>IADsService</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">Get</a>
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
<a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">GetInfo</a>
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
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsService</b> interface has these properties.
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

<a href="https://msdn.microsoft.com/ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8">Dependencies</a>


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

<a href="https://msdn.microsoft.com/ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8">DisplayName</a>


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

<a href="https://msdn.microsoft.com/ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8">ErrorControl</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">GUID</a>


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

<a href="https://msdn.microsoft.com/ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8">HostComputer</a>


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

<a href="https://msdn.microsoft.com/ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8">LoadOrderGroup</a>


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

<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">Name</a>


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

<a href="https://msdn.microsoft.com/ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8">Path</a>


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

<a href="https://msdn.microsoft.com/ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8">ServiceAccountName</a>


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

<a href="https://msdn.microsoft.com/ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8">ServiceAccountPath</a>


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

<a href="https://msdn.microsoft.com/ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8">ServiceType</a>


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

<a href="https://msdn.microsoft.com/ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8">StartType</a>


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

<a href="https://msdn.microsoft.com/ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8">StartupParameters</a>


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

<a href="https://msdn.microsoft.com/ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8">Version</a>


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



The system services are published in the underlying directory. Some may be running, others may not. To verify the status or to operate on any of the services, use the properties and methods of the  <a href="https://msdn.microsoft.com/f2459ca2-8a14-4343-bec6-ef3775dbf415">IADsServiceOperations</a> interface.

File service is a special case of the system service. The  <a href="https://msdn.microsoft.com/328eedfe-7fdc-4e90-8bac-ab30944b8fbf">IADsFileService</a> and  <a href="https://msdn.microsoft.com/91335658-8efb-4945-9862-f72e78d749d6">IADsFileServiceOperations</a> interfaces support additional features unique to file services.


#### Examples

To identify services available on a host computer, first bind to the computer and then enumerate the services available on that computer. The following code example shows  how to do this.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Public Sub ListServicesOnComputer(ComputerName As String)
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
    If (Err.Number &lt;&gt; 0) Then
        MsgBox (Err.Description &amp; vbLf &amp; vbLf &amp; " Error number = " &amp; Err.Number)
    End If
    Set comp = Nothing
End Sub</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/328eedfe-7fdc-4e90-8bac-ab30944b8fbf">IADsFileService</a>



<a href="https://msdn.microsoft.com/91335658-8efb-4945-9862-f72e78d749d6">IADsFileServiceOperations</a>



<a href="https://msdn.microsoft.com/ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8">IADsService Property Methods</a>



<a href="https://msdn.microsoft.com/f2459ca2-8a14-4343-bec6-ef3775dbf415">IADsServiceOperations</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 


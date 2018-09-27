---
UID: NN:iads.IADsFileServiceOperations
title: IADsFileServiceOperations
author: windows-sdk-content
description: The IADsFileServiceOperations interface is a dual interface that inherits from IADsServiceOperations.
old-location: adsi\iadsfileserviceoperations.htm
tech.root: ADSI
ms.assetid: 91335658-8efb-4945-9862-f72e78d749d6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IADsFileServiceOperations, IADsFileServiceOperations interface [ADSI], IADsFileServiceOperations interface [ADSI],described, _ds_iadsfileserviceoperations, adsi.iadsfileserviceoperations, iads/IADsFileServiceOperations
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
 - IADsFileServiceOperations
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsFileServiceOperations interface


## -description


The <b>IADsFileServiceOperations</b> interface is a dual interface that inherits from <a href="https://msdn.microsoft.com/f2459ca2-8a14-4343-bec6-ef3775dbf415">IADsServiceOperations</a>. It extends the functionality, as exposed in the  <b>IADsServiceOperations</b> interface, for managing the file service across a network. Specifically, it serves to maintain and manage open resources and active sessions of the file service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsFileServiceOperations</b> interface inherits from <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>, <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>, and <a href="https://msdn.microsoft.com/f2459ca2-8a14-4343-bec6-ef3775dbf415">IADsServiceOperations</a>. <b>IADsFileServiceOperations</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsFileServiceOperations</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de7627b4-8873-4324-b833-ff4cf018a428">Continue</a>
</td>
<td align="left" width="63%">
Continues the service.

</td>
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
<a href="https://msdn.microsoft.com/119ad6df-551c-48f9-8ad4-0ab18f5d939c">Pause</a>
</td>
<td align="left" width="63%">
Pauses the service.

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
<a href="https://msdn.microsoft.com/5b7f2240-ca92-4e8e-b3ec-8eab36c3166f">Resources</a>
</td>
<td align="left" width="63%">
Gets an interface pointer on a collection object that represents current open resources for this file service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97b485c9-650a-4d87-adbb-51799581c3bc">Sessions</a>
</td>
<td align="left" width="63%">
Gets an interface pointer on a collection object that represents current open sessions on this file service.

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
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a10684d1-be61-4599-b232-638b416aa127">SetPassword</a>
</td>
<td align="left" width="63%">
Sets the password to be used by the service manager to create a security context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8eabd59e-2abf-4e6f-be42-342f3b722d75">Start</a>
</td>
<td align="left" width="63%">
Starts the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e3b6c3e-0621-4760-8751-15f084b3aaa6">Stop</a>
</td>
<td align="left" width="63%">
Stops the service.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsFileServiceOperations</b> interface has these properties.
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

<a href="https://msdn.microsoft.com/ebddfc42-1d2f-495b-b57c-f57419b54ff8">Status</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the status of the service.

</td>
</tr>
</table> 


## -remarks



To bind to a file service operations object, use the ADsPath string that identifies the "LanmanServer" service on the host computer, as shown in the following code example.


```vb
Dim fso As IADsFileServiceOperations
On Error Resume Next

' Replace aDomain with the domain that the computer is located on.
' Replace aComputer with the name of the computer.
Set fso = GetObject("WinNT://aDomain/aComputer/LanmanServer")
```


From this point, you can handle the file service object as just a service object, applying any of the methods of <a href="https://msdn.microsoft.com/f2459ca2-8a14-4343-bec6-ef3775dbf415">IADsServiceOperations</a> to the file service object. For example, you can examine the operational status of the file service, start or stop the file service, or change its password.

However, the <b>IADsFileServiceOperations</b> interface allows you to work with open resources and active sessions of the file service. See the following example.


```vb
For Each r in fso.Resources
MsgBox r.User
MsgBox r.Path
MsgBox r.LockCount
Next
```


For more information about active sessions and open resources, see  <a href="https://msdn.microsoft.com/54621f0d-7478-4a6f-a96f-f3f93e64b281">IADsSession</a> and  <a href="https://msdn.microsoft.com/217749a4-55dc-457f-8582-1513ff3b0666">IADsResource</a>.




## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/328eedfe-7fdc-4e90-8bac-ab30944b8fbf">IADsFileService</a>



<a href="https://msdn.microsoft.com/217749a4-55dc-457f-8582-1513ff3b0666">IADsResource</a>



<a href="https://msdn.microsoft.com/b59a6594-1109-4913-8a83-4888e56e71d0">IADsService</a>



<a href="https://msdn.microsoft.com/f2459ca2-8a14-4343-bec6-ef3775dbf415">IADsServiceOperations</a>



<a href="https://msdn.microsoft.com/54621f0d-7478-4a6f-a96f-f3f93e64b281">IADsSession</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 


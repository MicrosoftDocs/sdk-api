---
UID: NN:iads.IADsFileServiceOperations
title: IADsFileServiceOperations (iads.h)
author: windows-sdk-content
description: The IADsFileServiceOperations interface is a dual interface that inherits from IADsServiceOperations.
old-location: adsi\iadsfileserviceoperations.htm
tech.root: adsi
ms.assetid: 91335658-8efb-4945-9862-f72e78d749d6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IADsFileServiceOperations, IADsFileServiceOperations interface [ADSI], IADsFileServiceOperations interface [ADSI],described, _ds_iadsfileserviceoperations, adsi.iadsfileserviceoperations, iads/IADsFileServiceOperations
ms.topic: interface
f1_keywords: ["iads/IADsFileServiceOperations"]
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
ms.custom: 19H1
---

# IADsFileServiceOperations interface


## -description


The <b>IADsFileServiceOperations</b> interface is a dual interface that inherits from <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsserviceoperations">IADsServiceOperations</a>. It extends the functionality, as exposed in the  <b>IADsServiceOperations</b> interface, for managing the file service across a network. Specifically, it serves to maintain and manage open resources and active sessions of the file service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsFileServiceOperations</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>, <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsserviceoperations">IADsServiceOperations</a>. <b>IADsFileServiceOperations</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsserviceoperations-continue">Continue</a>
</td>
<td align="left" width="63%">
Continues the service.

</td>
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
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsserviceoperations-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses the service.

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
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsfileserviceoperations-resources">Resources</a>
</td>
<td align="left" width="63%">
Gets an interface pointer on a collection object that represents current open resources for this file service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsfileserviceoperations-sessions">Sessions</a>
</td>
<td align="left" width="63%">
Gets an interface pointer on a collection object that represents current open sessions on this file service.

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
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsserviceoperations-setpassword">SetPassword</a>
</td>
<td align="left" width="63%">
Sets the password to be used by the service manager to create a security context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsserviceoperations-start">Start</a>
</td>
<td align="left" width="63%">
Starts the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsserviceoperations-stop">Stop</a>
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

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsserviceoperations-property-methods">Status</a>


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


From this point, you can handle the file service object as just a service object, applying any of the methods of <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsserviceoperations">IADsServiceOperations</a> to the file service object. For example, you can examine the operational status of the file service, start or stop the file service, or change its password.

However, the <b>IADsFileServiceOperations</b> interface allows you to work with open resources and active sessions of the file service. See the following example.


```vb
For Each r in fso.Resources
MsgBox r.User
MsgBox r.Path
MsgBox r.LockCount
Next
```


For more information about active sessions and open resources, see  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadssession">IADsSession</a> and  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsresource">IADsResource</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsfileservice">IADsFileService</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsresource">IADsResource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsservice">IADsService</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsserviceoperations">IADsServiceOperations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadssession">IADsSession</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 


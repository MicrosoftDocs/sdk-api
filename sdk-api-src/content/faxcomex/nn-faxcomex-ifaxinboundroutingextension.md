---
UID: NN:faxcomex.IFaxInboundRoutingExtension
title: IFaxInboundRoutingExtension
author: windows-sdk-content
description: The IFaxInboundRoutingExtension interface defines a configuration object used by a fax client application to retrieve information about a fax routing extension registered with the fax service.
old-location: fax\_mfax_faxinboundroutingextension_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_0t66_cpp.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxInboundRoutingExtension, IFaxInboundRoutingExtension interface [Fax Service], IFaxInboundRoutingExtension interface [Fax Service],described, _mfax_faxinboundroutingextension_cpp, fax._mfax_faxinboundroutingextension_cpp, faxcomex/IFaxInboundRoutingExtension
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxInboundRoutingExtension
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxInboundRoutingExtension interface


## -description


The <b>IFaxInboundRoutingExtension</b> interface defines a configuration object used by a fax client application to retrieve information about a fax routing extension registered with the fax service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRoutingExtension</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxInboundRoutingExtension</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRoutingExtension</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7c47b4d4-269e-48fe-9a0f-951e0e5dbb01">Debug</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/7c47b4d4-269e-48fe-9a0f-951e0e5dbb01">IFaxInboundRoutingExtension::get_Debug</a> property is a Boolean value that indicates whether the fax routing extension DLL was created in a debug environment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/90f52d04-31c2-4b48-bb6d-ea068728b67e">FriendlyName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/90f52d04-31c2-4b48-bb6d-ea068728b67e">IFaxInboundRoutingExtension::get_FriendlyName</a> property is a null-terminated string that contains the user-friendly name for the fax routing extension. The string is suitable for display to users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn895612">ImageName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ace23017-9839-4c5c-a992-e038ae1c0635">IFaxInboundRoutingExtension::get_ImageName</a> property is a null-terminated string that contains the executable image name (DLL path and file name) of the fax routing extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/64aaac61-00ba-4888-b177-b847d8896e09">InitErrorCode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/64aaac61-00ba-4888-b177-b847d8896e09">IFaxInboundRoutingExtension::get_InitErrorCode</a> property is a value that specifies the last error code that the fax routing extension returned while the fax service was loading and initializing the fax routing extension's DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6a986b94-e09e-4ecc-a324-ee9df3705a11">MajorBuild</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6a986b94-e09e-4ecc-a324-ee9df3705a11">IFaxInboundRoutingExtension::get_MajorBuild</a> property is a value that specifies the major part of the build number for the fax routing extension's DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/028ed452-c76c-47a0-a3d7-40b60cf46a40">MajorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/028ed452-c76c-47a0-a3d7-40b60cf46a40">IFaxInboundRoutingExtension::get_MajorVersion</a> property is a value that specifies the major part of the version number for the fax routing extension's DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c56e55bf-b20e-4249-90d0-93e97333a0fb">Methods</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c56e55bf-b20e-4249-90d0-93e97333a0fb">IFaxInboundRoutingExtension::get_Methods</a> property is an array of GUIDs that uniquely identify the inbound routing methods exposed by the fax routing extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7674d008-f2c6-4f07-9d8e-28d32f57f7ad">MinorBuild</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/7674d008-f2c6-4f07-9d8e-28d32f57f7ad">IFaxInboundRoutingExtension::get_MinorBuild</a> property is a value that specifies the minor part of the build number for the fax routing extension's DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f448e715-623d-423b-a75a-43eef08fb7c3">MinorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f448e715-623d-423b-a75a-43eef08fb7c3">IFaxInboundRoutingExtension::get_MinorVersion</a> property is a value that specifies the minor part of the version number for the fax routing extension's DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/496b2216-8ec6-4de9-8829-13b8ec404514">IFaxInboundRoutingExtension::get_Status</a> property is a value that indicates whether the fax routing extension loaded and initialized successfully. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b9726d54-adec-466e-b47a-3a3bc0438adf">UniqueName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b9726d54-adec-466e-b47a-3a3bc0438adf">IFaxInboundRoutingExtension::get_UniqueName</a> property is a null-terminated string that contains a unique name for the fax routing extension. The fax service uses this name internally to identify fax routing extensions.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxInboundRoutingExtension</b> is provided as the <a href="https://msdn.microsoft.com/cb875610-d6c9-473d-b9c2-0035e67a8949">FaxInboundRoutingExtension</a> object.




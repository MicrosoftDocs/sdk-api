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
req.redist: 
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRoutingExtension</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxInboundRoutingExtension</b> also has these types of members:
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

<a href="https://msdn.microsoft.com/en-us/library/ms686785(v=VS.85).aspx">Debug</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686785(v=VS.85).aspx">IFaxInboundRoutingExtension::get_Debug</a> property is a Boolean value that indicates whether the fax routing extension DLL was created in a debug environment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686170(v=VS.85).aspx">FriendlyName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686170(v=VS.85).aspx">IFaxInboundRoutingExtension::get_FriendlyName</a> property is a null-terminated string that contains the user-friendly name for the fax routing extension. The string is suitable for display to users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ace23017-9839-4c5c-a992-e038ae1c0635">ImageName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684599(v=VS.85).aspx">IFaxInboundRoutingExtension::get_ImageName</a> property is a null-terminated string that contains the executable image name (DLL path and file name) of the fax routing extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687447(v=VS.85).aspx">InitErrorCode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687447(v=VS.85).aspx">IFaxInboundRoutingExtension::get_InitErrorCode</a> property is a value that specifies the last error code that the fax routing extension returned while the fax service was loading and initializing the fax routing extension's DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms684564(v=VS.85).aspx">MajorBuild</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684564(v=VS.85).aspx">IFaxInboundRoutingExtension::get_MajorBuild</a> property is a value that specifies the major part of the build number for the fax routing extension's DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686716(v=VS.85).aspx">MajorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686716(v=VS.85).aspx">IFaxInboundRoutingExtension::get_MajorVersion</a> property is a value that specifies the major part of the version number for the fax routing extension's DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">IFaxInboundRoutingExtension::get_Methods</a> property is an array of GUIDs that uniquely identify the inbound routing methods exposed by the fax routing extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686747(v=VS.85).aspx">MinorBuild</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686747(v=VS.85).aspx">IFaxInboundRoutingExtension::get_MinorBuild</a> property is a value that specifies the minor part of the build number for the fax routing extension's DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms684813(v=VS.85).aspx">MinorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684813(v=VS.85).aspx">IFaxInboundRoutingExtension::get_MinorVersion</a> property is a value that specifies the minor part of the version number for the fax routing extension's DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/496b2216-8ec6-4de9-8829-13b8ec404514">Status</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687475(v=VS.85).aspx">IFaxInboundRoutingExtension::get_Status</a> property is a value that indicates whether the fax routing extension loaded and initialized successfully. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms685212(v=VS.85).aspx">UniqueName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms685212(v=VS.85).aspx">IFaxInboundRoutingExtension::get_UniqueName</a> property is a null-terminated string that contains a unique name for the fax routing extension. The fax service uses this name internally to identify fax routing extensions.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxInboundRoutingExtension</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/ms684580(v=VS.85).aspx">FaxInboundRoutingExtension</a> object.




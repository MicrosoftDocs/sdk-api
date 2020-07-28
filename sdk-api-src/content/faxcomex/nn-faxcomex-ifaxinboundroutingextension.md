---
UID: NN:faxcomex.IFaxInboundRoutingExtension
title: IFaxInboundRoutingExtension (faxcomex.h)
description: The IFaxInboundRoutingExtension interface defines a configuration object used by a fax client application to retrieve information about a fax routing extension registered with the fax service.
helpviewer_keywords: ["IFaxInboundRoutingExtension","IFaxInboundRoutingExtension interface [Fax Service]","IFaxInboundRoutingExtension interface [Fax Service]","described","_mfax_faxinboundroutingextension_cpp","fax._mfax_faxinboundroutingextension_cpp","faxcomex/IFaxInboundRoutingExtension"]
old-location: fax\_mfax_faxinboundroutingextension_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_0t66_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxInboundRoutingExtension, IFaxInboundRoutingExtension interface [Fax Service], IFaxInboundRoutingExtension interface [Fax Service],described, _mfax_faxinboundroutingextension_cpp, fax._mfax_faxinboundroutingextension_cpp, faxcomex/IFaxInboundRoutingExtension
f1_keywords:
- faxcomex/IFaxInboundRoutingExtension
dev_langs:
- c++
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Fxscomex.dll
api_name:
- IFaxInboundRoutingExtension
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxInboundRoutingExtension interface


## -description


The <b>IFaxInboundRoutingExtension</b> interface defines a configuration object used by a fax client application to retrieve information about a fax routing extension registered with the fax service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxInboundRoutingExtension</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxInboundRoutingExtension</b> also has these types of members:
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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-debug-vb">Debug</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-debug-vb">IFaxInboundRoutingExtension::get_Debug</a> property is a Boolean value that indicates whether the fax routing extension DLL was created in a debug environment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-friendlyname-vb">FriendlyName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-friendlyname-vb">IFaxInboundRoutingExtension::get_FriendlyName</a> property is a null-terminated string that contains the user-friendly name for the fax routing extension. The string is suitable for display to users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-imagename-vb">ImageName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-imagename-vb">IFaxInboundRoutingExtension::get_ImageName</a> property is a null-terminated string that contains the executable image name (DLL path and file name) of the fax routing extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-initerrorcode-vb">InitErrorCode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-initerrorcode-vb">IFaxInboundRoutingExtension::get_InitErrorCode</a> property is a value that specifies the last error code that the fax routing extension returned while the fax service was loading and initializing the fax routing extension's DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-majorbuild-vb">MajorBuild</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-majorbuild-vb">IFaxInboundRoutingExtension::get_MajorBuild</a> property is a value that specifies the major part of the build number for the fax routing extension's DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-majorversion-vb">MajorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-majorversion-vb">IFaxInboundRoutingExtension::get_MajorVersion</a> property is a value that specifies the major part of the version number for the fax routing extension's DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-methods-vb">Methods</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-methods-vb">IFaxInboundRoutingExtension::get_Methods</a> property is an array of GUIDs that uniquely identify the inbound routing methods exposed by the fax routing extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-minorbuild-vb">MinorBuild</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-minorbuild-vb">IFaxInboundRoutingExtension::get_MinorBuild</a> property is a value that specifies the minor part of the build number for the fax routing extension's DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-minorversion-vb">MinorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-minorversion-vb">IFaxInboundRoutingExtension::get_MinorVersion</a> property is a value that specifies the minor part of the version number for the fax routing extension's DLL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-status-vb">Status</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-status-vb">IFaxInboundRoutingExtension::get_Status</a> property is a value that indicates whether the fax routing extension loaded and initialized successfully. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-uniquename-vb">UniqueName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension-uniquename-vb">IFaxInboundRoutingExtension::get_UniqueName</a> property is a null-terminated string that contains a unique name for the fax routing extension. The fax service uses this name internally to identify fax routing extensions.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxInboundRoutingExtension</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension">FaxInboundRoutingExtension</a> object.




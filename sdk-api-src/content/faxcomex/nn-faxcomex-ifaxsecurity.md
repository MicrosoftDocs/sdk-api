---
UID: NN:faxcomex.IFaxSecurity
title: IFaxSecurity
author: windows-sdk-content
description: The IFaxSecurity configuration object is used by a fax client application to configure the security on a fax server, and permits the calling application to set and retrieve a security descriptor for the fax server.
old-location: fax\_mfax_faxsecurity_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_63cp_cpp.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxSecurity, IFaxSecurity interface [Fax Service], IFaxSecurity interface [Fax Service],described, _mfax_faxsecurity_cpp, fax._mfax_faxsecurity_cpp, faxcomex/IFaxSecurity
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
 - IFaxSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxSecurity interface


## -description


The <b>IFaxSecurity</b> configuration object is used by a fax client application to configure the security on a fax server, and permits the calling application to set and retrieve a security descriptor for the fax server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxSecurity</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxSecurity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxSecurity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms690274(v=VS.85).aspx">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690274(v=VS.85).aspx">IFaxSecurity::Refresh</a> method refreshes <a href="https://msdn.microsoft.com/en-us/library/ms689509(v=VS.85).aspx">FaxSecurity</a> object information from the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms690247(v=VS.85).aspx">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms690247(v=VS.85).aspx">IFaxSecurity::Save</a> method saves the <a href="https://msdn.microsoft.com/en-us/library/ms689509(v=VS.85).aspx">FaxSecurity</a> object data.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxSecurity</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa358834(v=VS.85).aspx">Descriptor</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/Aa358834(v=VS.85).aspx">Descriptor</a> property  represents the security descriptor for a <a href="https://msdn.microsoft.com/en-us/library/ms689110(v=VS.85).aspx">IFaxServer</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689128(v=VS.85).aspx">get_InformationType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689128(v=VS.85).aspx">IFaxSecurity::InformationType</a> property represents the security information type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms689131(v=VS.85).aspx">GrantedRights</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms689131(v=VS.85).aspx">IFaxSecurity::get_GrantedRights</a> property is a combination of the fax server access rights granted to the user referencing this property. For example, some users have permission to submit fax jobs with high priority while others have permission to submit jobs with normal or low priority only.

</td>
</tr>
</table> 


## -remarks



Only an administrator with permissions can configure the security of the fax server. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb442405(v=VS.85).aspx">Access Control</a>.

A default implementation of <b>IFaxSecurity</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/ms689509(v=VS.85).aspx">FaxSecurity</a> object.




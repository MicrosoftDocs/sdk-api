---
UID: NN:wia_xp.IEnumWIA_FORMAT_INFO
title: IEnumWIA_FORMAT_INFO (wia_xp.h)
author: windows-sdk-content
description: Use the IEnumWIA_FORMAT_INFO interface to enumerate the format and media type information for a device.
old-location: wia\_wia_IEnumWIA_FORMAT_INFO.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwia_format_info\ienumwia_format_info.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumWIA_FORMAT_INFO, IEnumWIA_FORMAT_INFO interface [WIA], IEnumWIA_FORMAT_INFO interface [WIA],described, _wia_IEnumWIA_FORMAT_INFO, wia._wia_IEnumWIA_FORMAT_INFO, wia_xp/IEnumWIA_FORMAT_INFO
ms.topic: interface
f1_keywords:
- wia_xp/IEnumWIA_FORMAT_INFO
dev_langs:
 - c++
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: Wiaguid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
api_name:
- IEnumWIA_FORMAT_INFO
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumWIA_FORMAT_INFO interface


## -description


Use the <b>IEnumWIA_FORMAT_INFO</b> interface to enumerate the format and media type information for a device.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumWIA_FORMAT_INFO</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumWIA_FORMAT_INFO</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumWIA_FORMAT_INFO</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_format_info-clone">Clone</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_format_info-clone">IEnumWIA_FORMAT_INFO::Clone</a> method creates an additional instance of the <b>IEnumWIA_FORMAT_INFO</b> interface and returns an interface pointer to the new interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_format_info-getcount">GetCount</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_format_info-getcount">IEnumWIA_FORMAT_INFO::GetCount</a> method returns the number of elements stored by this enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_format_info-next">Next</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_format_info-next">IEnumWIA_FORMAT_INFO::Next</a> method returns an array of <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/ns-wia_xp-wia_format_info">WIA_FORMAT_INFO</a> structures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_format_info-reset">Reset</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_format_info-reset">IEnumWIA_FORMAT_INFO::Reset</a> method sets the enumeration back to the first <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/ns-wia_xp-wia_format_info">WIA_FORMAT_INFO</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_format_info-skip">Skip</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_format_info-skip">IEnumWIA_FORMAT_INFO::Skip</a> method skips the specified number of structures in the enumeration.

</td>
</tr>
</table> 


## -remarks



The <b>IEnumWIA_FORMAT_INFO</b> interface is a specific implementation for Windows Image Acquisition (WIA) of the standard Component Object Model (COM) enumeration interface. For details, see <a href="https://docs.microsoft.com/previous-versions/ms680089(v=vs.85)">IEnumXXXX</a>.

Applications obtain a pointer to the <b>IEnumWIA_FORMAT_INFO</b> interface by invoking the <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info">IWiaDataTransfer::idtEnumWIA_FORMAT_INFO</a> method of an item's <a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer">IWiaDataTransfer</a> interface.

The <b>IEnumWIA_FORMAT_INFO</b> interface, like all COM interfaces, inherits the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods. 

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/ms680089(v=vs.85)">IEnumXXXX</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info">idtEnumWIA_FORMAT_INFO</a>
 

 


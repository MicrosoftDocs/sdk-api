---
UID: NN:wia_xp.IEnumWIA_FORMAT_INFO
title: IEnumWIA_FORMAT_INFO (wia_xp.h)
description: Use the IEnumWIA_FORMAT_INFO interface to enumerate the format and media type information for a device.
helpviewer_keywords: ["IEnumWIA_FORMAT_INFO","IEnumWIA_FORMAT_INFO interface [WIA]","IEnumWIA_FORMAT_INFO interface [WIA]","described","_wia_IEnumWIA_FORMAT_INFO","wia._wia_IEnumWIA_FORMAT_INFO","wia_xp/IEnumWIA_FORMAT_INFO"]
old-location: wia\_wia_IEnumWIA_FORMAT_INFO.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwia_format_info\ienumwia_format_info.htm
ms.date: 12/05/2018
ms.keywords: IEnumWIA_FORMAT_INFO, IEnumWIA_FORMAT_INFO interface [WIA], IEnumWIA_FORMAT_INFO interface [WIA],described, _wia_IEnumWIA_FORMAT_INFO, wia._wia_IEnumWIA_FORMAT_INFO, wia_xp/IEnumWIA_FORMAT_INFO
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumWIA_FORMAT_INFO
 - wia_xp/IEnumWIA_FORMAT_INFO
dev_langs:
 - c++
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
archived: true
---

# IEnumWIA_FORMAT_INFO interface


## -description

Use the <b>IEnumWIA_FORMAT_INFO</b> interface to enumerate the format and media type information for a device.

## -inheritance

The <b>IEnumWIA_FORMAT_INFO</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumWIA_FORMAT_INFO</b> also has these types of members:

## -remarks

The <b>IEnumWIA_FORMAT_INFO</b> interface is a specific implementation for Windows Image Acquisition (WIA) of the standard Component Object Model (COM) enumeration interface. For details, see <a href="/previous-versions/ms680089(v=vs.85)">IEnumXXXX</a>.

Applications obtain a pointer to the <b>IEnumWIA_FORMAT_INFO</b> interface by invoking the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info">IWiaDataTransfer::idtEnumWIA_FORMAT_INFO</a> method of an item's <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer">IWiaDataTransfer</a> interface.

The <b>IEnumWIA_FORMAT_INFO</b> interface, like all COM interfaces, inherits the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods. 

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/ms680089(v=vs.85)">IEnumXXXX</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtenumwia_format_info">idtEnumWIA_FORMAT_INFO</a>

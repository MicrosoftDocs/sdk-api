---
UID: NN:wia_xp.IEnumWIA_DEV_CAPS
title: IEnumWIA_DEV_CAPS (wia_xp.h)
description: The IEnumWIA_DEV_CAPS interface enumerates the currently available Windows Image Acquisition (WIA) hardware device capabilities. Device capabilities include commands and events that the device supports.
helpviewer_keywords: ["IEnumWIA_DEV_CAPS","IEnumWIA_DEV_CAPS interface [WIA]","IEnumWIA_DEV_CAPS interface [WIA]","described","_wia_IEnumWIA_DEV_CAPS","wia._wia_IEnumWIA_DEV_CAPS","wia_xp/IEnumWIA_DEV_CAPS"]
old-location: wia\_wia_IEnumWIA_DEV_CAPS.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwia_dev_caps\ienumwia_dev_caps.htm
ms.date: 12/05/2018
ms.keywords: IEnumWIA_DEV_CAPS, IEnumWIA_DEV_CAPS interface [WIA], IEnumWIA_DEV_CAPS interface [WIA],described, _wia_IEnumWIA_DEV_CAPS, wia._wia_IEnumWIA_DEV_CAPS, wia_xp/IEnumWIA_DEV_CAPS
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
 - IEnumWIA_DEV_CAPS
 - wia_xp/IEnumWIA_DEV_CAPS
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
 - IEnumWIA_DEV_CAPS
archived: true
---

# IEnumWIA_DEV_CAPS interface


## -description

The <b>IEnumWIA_DEV_CAPS</b> interface enumerates the currently available Windows Image Acquisition (WIA) hardware device capabilities. Device capabilities include commands and events that the device supports.

## -inheritance

The <b>IEnumWIA_DEV_CAPS</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumWIA_DEV_CAPS</b> also has these types of members:

## -remarks

The <b>IEnumWIA_DEV_CAPS</b> interface is a specific implementation for WIA of the standard OLE enumeration interface. For details, see <a href="/previous-versions/ms680089(v=vs.85)">IEnumXXXX</a>.

Applications obtain a pointer to the <b>IEnumWIA_DEV_CAPS</b> interface by invoking the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities">IWiaItem::EnumDeviceCapabilities</a> method.

The <b>IEnumWIA_DEV_CAPS</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods.

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

<a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities">EnumDeviceCapabilities</a>



<a href="/previous-versions/ms680089(v=vs.85)">IEnumXXXX</a>



<b>Other Resources</b>



<b>Reference</b>

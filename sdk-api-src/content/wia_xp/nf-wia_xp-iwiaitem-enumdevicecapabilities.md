---
UID: NF:wia_xp.IWiaItem.EnumDeviceCapabilities
title: IWiaItem::EnumDeviceCapabilities (wia_xp.h)
description: The IWiaItem::EnumDeviceCapabilities method creates an enumerator that is used to ascertain the commands and events a Windows Image Acquisition (WIA) device supports.
helpviewer_keywords: ["EnumDeviceCapabilities","EnumDeviceCapabilities method [WIA]","EnumDeviceCapabilities method [WIA]","IWiaItem interface","IWiaItem interface [WIA]","EnumDeviceCapabilities method","IWiaItem.EnumDeviceCapabilities","IWiaItem::EnumDeviceCapabilities","_wia_IWiaItem_EnumDeviceCapabilities","wia._wia_IWiaItem_EnumDeviceCapabilities","wia_xp/IWiaItem::EnumDeviceCapabilities"]
old-location: wia\_wia_IWiaItem_EnumDeviceCapabilities.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\enumdevicecapabilities.htm
ms.date: 12/05/2018
ms.keywords: EnumDeviceCapabilities, EnumDeviceCapabilities method [WIA], EnumDeviceCapabilities method [WIA],IWiaItem interface, IWiaItem interface [WIA],EnumDeviceCapabilities method, IWiaItem.EnumDeviceCapabilities, IWiaItem::EnumDeviceCapabilities, _wia_IWiaItem_EnumDeviceCapabilities, wia._wia_IWiaItem_EnumDeviceCapabilities, wia_xp/IWiaItem::EnumDeviceCapabilities
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
req.dll: Wiaservc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWiaItem::EnumDeviceCapabilities
 - wia_xp/IWiaItem::EnumDeviceCapabilities
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaItem.EnumDeviceCapabilities
archived: true
---

# IWiaItem::EnumDeviceCapabilities


## -description

The <b>IWiaItem::EnumDeviceCapabilities</b> method creates an enumerator that is used to ascertain the commands and events a Windows Image Acquisition (WIA) device supports.

## -parameters

### -param lFlags [in]

Type: <b>LONG</b>

Specifies a flag that selects the type of capabilities to enumerate. Can be set to one or more of the following values:



<table class="clsStd">
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>WIA_DEVICE_COMMANDS</td>
<td>Enumerate device commands.</td>
</tr>
<tr>
<td>WIA_DEVICE_EVENTS</td>
<td>Enumerate device events.</td>
</tr>
</table>

### -param ppIEnumWIA_DEV_CAPS [out]

Type: <b><a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps">IEnumWIA_DEV_CAPS</a>**</b>

Pointer to <a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps">IEnumWIA_DEV_CAPS</a> interface created by <b>IWiaItem::EnumDeviceCapabilities</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Use this method to create an enumerator object to obtain the set of commands and events that a WIA device supports. You can use the <i>lFlags</i> parameter to specify which kinds of device capabilities to enumerate. The <b>IWiaItem::EnumDeviceCapabilities</b> method stores the address of the interface of the enumerator object in the <i>ppIEnumWIA_DEV_CAPS</i> parameter.

Applications must call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIEnumWIA_DEV_CAPS</i> parameter.
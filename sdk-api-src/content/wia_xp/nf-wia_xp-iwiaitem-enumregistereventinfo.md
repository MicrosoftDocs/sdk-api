---
UID: NF:wia_xp.IWiaItem.EnumRegisterEventInfo
title: IWiaItem::EnumRegisterEventInfo (wia_xp.h)
description: The IWiaItem::EnumRegisterEventInfo method creates an enumerator used to obtain information about events for which an application is registered.
helpviewer_keywords: ["EnumRegisterEventInfo","EnumRegisterEventInfo method [WIA]","EnumRegisterEventInfo method [WIA]","IWiaItem interface","IWiaItem interface [WIA]","EnumRegisterEventInfo method","IWiaItem.EnumRegisterEventInfo","IWiaItem::EnumRegisterEventInfo","_wia_IWiaItem_EnumRegisterEventInfo","wia._wia_IWiaItem_EnumRegisterEventInfo","wia_xp/IWiaItem::EnumRegisterEventInfo"]
old-location: wia\_wia_IWiaItem_EnumRegisterEventInfo.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\enumregistereventinfo.htm
ms.date: 12/05/2018
ms.keywords: EnumRegisterEventInfo, EnumRegisterEventInfo method [WIA], EnumRegisterEventInfo method [WIA],IWiaItem interface, IWiaItem interface [WIA],EnumRegisterEventInfo method, IWiaItem.EnumRegisterEventInfo, IWiaItem::EnumRegisterEventInfo, _wia_IWiaItem_EnumRegisterEventInfo, wia._wia_IWiaItem_EnumRegisterEventInfo, wia_xp/IWiaItem::EnumRegisterEventInfo
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
 - IWiaItem::EnumRegisterEventInfo
 - wia_xp/IWiaItem::EnumRegisterEventInfo
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
 - IWiaItem.EnumRegisterEventInfo
archived: true
---

# IWiaItem::EnumRegisterEventInfo


## -description

The <b>IWiaItem::EnumRegisterEventInfo</b> method creates an enumerator used to obtain information about events for which an application is registered.

## -parameters

### -param lFlags [in]

Type: <b>LONG</b>

Currently unused. Should be set to zero.

### -param pEventGUID [in]

Type: <b>const GUID*</b>

Pointer to an identifier that specifies the hardware event for which you want registration information.

### -param ppIEnum [out]

Type: <b><a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps">IEnumWIA_DEV_CAPS</a>**</b>

Receives the address of a pointer to the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps">IEnumWIA_DEV_CAPS</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An application invokes this method to create an enumerator object for the event information. <b>IWiaItem::EnumRegisterEventInfo</b> stores the address of the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps">IEnumWIA_DEV_CAPS</a> interface of the enumerator object in the <i>ppIEnum</i> parameter. The program then uses the interface pointer to enumerate the properties of the event for which it is registered.

Each <a href="/windows/desktop/api/wia_xp/ns-wia_xp-wia_dev_cap">WIA_DEV_CAP</a> structure includes an indication of whether the event is of type WIA_NOTIFICATION_EVENT or WIA_ACTION_EVENT or both.

Applications must call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIEnum</i> parameter.
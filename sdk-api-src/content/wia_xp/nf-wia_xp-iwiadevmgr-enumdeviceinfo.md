---
UID: NF:wia_xp.IWiaDevMgr.EnumDeviceInfo
title: IWiaDevMgr::EnumDeviceInfo (wia_xp.h)
description: Applications use the IWiaDevMgr::EnumDeviceInfo method to enumerate property information for each available Windows Image Acquisition (WIA) device.
helpviewer_keywords: ["EnumDeviceInfo","EnumDeviceInfo method [WIA]","EnumDeviceInfo method [WIA]","IWiaDevMgr interface","IWiaDevMgr interface [WIA]","EnumDeviceInfo method","IWiaDevMgr.EnumDeviceInfo","IWiaDevMgr::EnumDeviceInfo","_wia_IWiaDevMgr_EnumDeviceInfo","wia._wia_IWiaDevMgr_EnumDeviceInfo","wia_xp/IWiaDevMgr::EnumDeviceInfo"]
old-location: wia\_wia_IWiaDevMgr_EnumDeviceInfo.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadevmgr\enumdeviceinfo.htm
ms.date: 12/05/2018
ms.keywords: EnumDeviceInfo, EnumDeviceInfo method [WIA], EnumDeviceInfo method [WIA],IWiaDevMgr interface, IWiaDevMgr interface [WIA],EnumDeviceInfo method, IWiaDevMgr.EnumDeviceInfo, IWiaDevMgr::EnumDeviceInfo, _wia_IWiaDevMgr_EnumDeviceInfo, wia._wia_IWiaDevMgr_EnumDeviceInfo, wia_xp/IWiaDevMgr::EnumDeviceInfo
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
 - IWiaDevMgr::EnumDeviceInfo
 - wia_xp/IWiaDevMgr::EnumDeviceInfo
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
 - IWiaDevMgr.EnumDeviceInfo
archived: true
---

# IWiaDevMgr::EnumDeviceInfo


## -description

Applications use the <b>IWiaDevMgr::EnumDeviceInfo</b> method to enumerate property information for each available Windows Image Acquisition (WIA) device.

## -parameters

### -param lFlag [in]

Type: <b>LONG</b>

Specifies the types of WIA devices to enumerate. Should be set to WIA_DEVINFO_ENUM_LOCAL.

### -param ppIEnum [out, retval]

Type: <b><a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info">IEnumWIA_DEV_INFO</a>**</b>

Receives the address of a pointer to the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info">IEnumWIA_DEV_INFO</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>IWiaDevMgr::EnumDeviceInfo</b> method creates an enumerator object, that supports the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info">IEnumWIA_DEV_INFO</a> interface. <b>IWiaDevMgr::EnumDeviceInfo</b> stores a pointer to the <b>IEnumWIA_DEV_INFO</b> interface in the parameter <i>ppIEnum</i>. Applications can use the <b>IEnumWIA_DEV_INFO</b> interface pointer to enumerate the properties of each WIA device attached to the user's computer.

Applications must call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIEnum</i> parameter.
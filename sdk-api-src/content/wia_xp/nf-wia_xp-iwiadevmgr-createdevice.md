---
UID: NF:wia_xp.IWiaDevMgr.CreateDevice
title: IWiaDevMgr::CreateDevice (wia_xp.h)
description: The IWiaDevMgr::CreateDevice creates a hierarchical tree of IWiaItem objects for a Windows Image Acquisition (WIA) device.
helpviewer_keywords: ["CreateDevice","CreateDevice method [WIA]","CreateDevice method [WIA]","IWiaDevMgr interface","IWiaDevMgr interface [WIA]","CreateDevice method","IWiaDevMgr.CreateDevice","IWiaDevMgr::CreateDevice","_wia_IWiaDevMgr_CreateDevice","wia._wia_IWiaDevMgr_CreateDevice","wia_xp/IWiaDevMgr::CreateDevice"]
old-location: wia\_wia_IWiaDevMgr_CreateDevice.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadevmgr\createdevice.htm
ms.date: 12/05/2018
ms.keywords: CreateDevice, CreateDevice method [WIA], CreateDevice method [WIA],IWiaDevMgr interface, IWiaDevMgr interface [WIA],CreateDevice method, IWiaDevMgr.CreateDevice, IWiaDevMgr::CreateDevice, _wia_IWiaDevMgr_CreateDevice, wia._wia_IWiaDevMgr_CreateDevice, wia_xp/IWiaDevMgr::CreateDevice
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
 - IWiaDevMgr::CreateDevice
 - wia_xp/IWiaDevMgr::CreateDevice
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
 - IWiaDevMgr.CreateDevice
archived: true
---

# IWiaDevMgr::CreateDevice


## -description

The <b>IWiaDevMgr::CreateDevice</b> creates a hierarchical tree of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> objects for a Windows Image Acquisition (WIA) device.

## -parameters

### -param bstrDeviceID [in]

Type: <b>BSTR</b>

Specifies the unique identifier of the WIA device.

### -param ppWiaItemRoot [out]

Type: <b><a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a>**</b>

Pointer to a pointer to the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> interface of the root item in the hierarchical tree for the WIA device.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Applications use the <b>IWiaDevMgr::CreateDevice</b> method to create a device object for the WIA devices specified by the <i>bstrDeviceID</i> parameter. 

When it returns, the <b>IWiaDevMgr::CreateDevice</b> method stores an address of a pointer in the parameter <i>ppWiaItemRoot</i>. The pointer points to the root item of the tree of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> objects created by <b>IWiaDevMgr::CreateDevice</b>. Applications can use this tree of objects to control and retrieve data from the WIA device.

Note that applications must call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on the pointers they receive through the <i>ppWiaItemRoot</i> parameter.
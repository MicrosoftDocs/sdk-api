---
UID: NF:wia_xp.IWiaEventCallback.ImageEventCallback
title: IWiaEventCallback::ImageEventCallback (wia_xp.h)
description: The IWiaEventCallback::ImageEventCallback method is invoked by the Windows Image Acquisition (WIA) run-time system when a hardware device event occurs.
helpviewer_keywords: ["IWiaEventCallback interface [WIA]","ImageEventCallback method","IWiaEventCallback.ImageEventCallback","IWiaEventCallback::ImageEventCallback","ImageEventCallback","ImageEventCallback method [WIA]","ImageEventCallback method [WIA]","IWiaEventCallback interface","_wia_IWiaEventCallback_ImageEventCallback","wia._wia_IWiaEventCallback_ImageEventCallback","wia_xp/IWiaEventCallback::ImageEventCallback"]
old-location: wia\_wia_IWiaEventCallback_ImageEventCallback.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaeventcallback\imageeventcallback.htm
ms.date: 12/05/2018
ms.keywords: IWiaEventCallback interface [WIA],ImageEventCallback method, IWiaEventCallback.ImageEventCallback, IWiaEventCallback::ImageEventCallback, ImageEventCallback, ImageEventCallback method [WIA], ImageEventCallback method [WIA],IWiaEventCallback interface, _wia_IWiaEventCallback_ImageEventCallback, wia._wia_IWiaEventCallback_ImageEventCallback, wia_xp/IWiaEventCallback::ImageEventCallback
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
 - IWiaEventCallback::ImageEventCallback
 - wia_xp/IWiaEventCallback::ImageEventCallback
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
 - IWiaEventCallback.ImageEventCallback
archived: true
---

# IWiaEventCallback::ImageEventCallback


## -description

The <b>IWiaEventCallback::ImageEventCallback</b> method is invoked by the Windows Image Acquisition (WIA) run-time system when a hardware device event occurs.

## -parameters

### -param pEventGUID [in]

Type: <b>const GUID*</b>

Specifies the unique identifier of the event. For a complete list of device events, see <a href="/windows/desktop/wia/-wia-wia-event-identifiers">WIA Event Identifiers</a>.

### -param bstrEventDescription [in]

Type: <b>BSTR</b>

Specifies the string description of the event.

### -param bstrDeviceID [in]

Type: <b>BSTR</b>

Specifies the unique identifier of the WIA device.

### -param bstrDeviceDescription [in]

Type: <b>BSTR</b>

Specifies the string description of the device.

### -param dwDeviceType [in]

Type: <b>DWORD</b>

Specifies the type of the device. See <a href="/windows/desktop/wia/-wia-wia-device-type-specifiers">WIA Device Type Specifiers</a> for a list of possible values.

### -param bstrFullItemName [in]

Type: <b>BSTR</b>

Specifies the full name of the WIA item that represents the device.

### -param pulEventType [in, out]

Type: <b>ULONG*</b>

Pointer to a <b>ULONG</b> that specifies whether an event is a notification event, an action event, or both. A value of 1 indicates a notification event, a value of 2 indicates an action event, and a value of 3 indicates that the event is of both notification and action type.

### -param ulReserved [in]

Type: <b>ULONG</b>

Reserved for user information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To receive notification of WIA hardware device events, applications pass a pointer to the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback">IWiaEventCallback</a> interface to the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface">RegisterEventCallbackInterface</a> method. The WIA run-time system then uses that interface pointer to invoke the <b>IWiaEventCallback::ImageEventCallback</b> method whenever a WIA hardware device event occurs.

Note that there is no guarantee the callback will be invoked on the same thread that registered the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback">IWiaEventCallback</a> interface.
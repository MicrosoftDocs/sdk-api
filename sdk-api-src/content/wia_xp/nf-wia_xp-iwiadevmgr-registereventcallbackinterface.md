---
UID: NF:wia_xp.IWiaDevMgr.RegisterEventCallbackInterface
title: IWiaDevMgr::RegisterEventCallbackInterface (wia_xp.h)
description: The IWiaDevMgr::RegisterEventCallbackInterface method registers a running application Windows Image Acquisition (WIA) event notification.
helpviewer_keywords: ["IWiaDevMgr interface [WIA]","RegisterEventCallbackInterface method","IWiaDevMgr.RegisterEventCallbackInterface","IWiaDevMgr::RegisterEventCallbackInterface","RegisterEventCallbackInterface","RegisterEventCallbackInterface method [WIA]","RegisterEventCallbackInterface method [WIA]","IWiaDevMgr interface","_wia_IWiaDevMgr_RegisterEventCallbackInterface","wia._wia_IWiaDevMgr_RegisterEventCallbackInterface","wia_xp/IWiaDevMgr::RegisterEventCallbackInterface"]
old-location: wia\_wia_IWiaDevMgr_RegisterEventCallbackInterface.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadevmgr\registereventcallbackinterface.htm
ms.date: 12/05/2018
ms.keywords: IWiaDevMgr interface [WIA],RegisterEventCallbackInterface method, IWiaDevMgr.RegisterEventCallbackInterface, IWiaDevMgr::RegisterEventCallbackInterface, RegisterEventCallbackInterface, RegisterEventCallbackInterface method [WIA], RegisterEventCallbackInterface method [WIA],IWiaDevMgr interface, _wia_IWiaDevMgr_RegisterEventCallbackInterface, wia._wia_IWiaDevMgr_RegisterEventCallbackInterface, wia_xp/IWiaDevMgr::RegisterEventCallbackInterface
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
 - IWiaDevMgr::RegisterEventCallbackInterface
 - wia_xp/IWiaDevMgr::RegisterEventCallbackInterface
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
 - IWiaDevMgr.RegisterEventCallbackInterface
archived: true
---

# IWiaDevMgr::RegisterEventCallbackInterface


## -description

The <b>IWiaDevMgr::RegisterEventCallbackInterface</b> method registers a running application Windows Image Acquisition (WIA) event notification.

## -parameters

### -param lFlags [in]

Type: <b>LONG</b>

Currently unused. Should be set to zero.

### -param bstrDeviceID [in]

Type: <b>BSTR</b>

Specifies a device identifier. Pass <b>NULL</b> to register for the event on all WIA devices.

### -param pEventGUID [in]

Type: <b>const GUID*</b>

Specifies the event for which the application is registering. For a list of standard events, see <a href="/windows/desktop/wia/-wia-wia-event-identifiers">WIA Event Identifiers</a>.

### -param pIWiaEventCallback [in]

Type: <b><a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback">IWiaEventCallback</a>*</b>

Pointer to the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback">IWiaEventCallback</a> interface that the WIA system used to send the event notification.

### -param pEventObject [out]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

Receives the address of a pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Warning</b>  Using the <b>IWiaDevMgr::RegisterEventCallbackInterface</b>, <a href="/windows/desktop/wia/-wia-iwiadevmgr2-registereventcallbackinterface">IWiaDevMgr2::RegisterEventCallbackInterface</a>, and <a href="/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent">DeviceManager.RegisterEvent</a> methods from the same process after the Still Image Service is restarted may cause an access violation, if the functions were used before the service was stopped.</div>
<div> </div>
When they begin executing, WIA applications use this method to register to receive hardware device events of the type WIA_NOTIFICATION_EVENT. This prevents the application from being restarted when another event for which it is registered occurs. Once a program invokes <b>IWiaDevMgr::RegisterEventCallbackInterface</b> to register itself to receive WIA events from a device, the registered events are routed to the program by the WIA system. 

Applications use the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo">EnumRegisterEventInfo</a> method to retrieve a pointer to an enumerator object for event registration properties.

An application can find whether an event is an action type or notification type (or both) event by examining the <b>ulFlags</b> value of a <a href="/windows/desktop/api/wia_xp/ns-wia_xp-wia_dev_cap">WIA_DEV_CAP</a> structure returned by event enumeration.

Applications can unregister for events by using the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer returned through the <i>pEventObject</i>  parameter to call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

<div class="alert"><b>Note</b>  In a multi-threaded application, there is no guarantee that the event notification callback will come in on the same thread that registered the callback.</div>
<div> </div>
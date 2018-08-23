---
UID: NF:wia_xp.IWiaDevMgr.RegisterEventCallbackInterface
title: IWiaDevMgr::RegisterEventCallbackInterface
author: windows-sdk-content
description: The IWiaDevMgr::RegisterEventCallbackInterface method registers a running application Windows Image Acquisition (WIA) event notification.
old-location: wia\_wia_IWiaDevMgr_RegisterEventCallbackInterface.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadevmgr\registereventcallbackinterface.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWiaDevMgr interface [WIA],RegisterEventCallbackInterface method, IWiaDevMgr.RegisterEventCallbackInterface, IWiaDevMgr::RegisterEventCallbackInterface, RegisterEventCallbackInterface, RegisterEventCallbackInterface method [WIA], RegisterEventCallbackInterface method [WIA],IWiaDevMgr interface, _wia_IWiaDevMgr_RegisterEventCallbackInterface, wia._wia_IWiaDevMgr_RegisterEventCallbackInterface, wia_xp/IWiaDevMgr::RegisterEventCallbackInterface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wia_xp.h
req.include-header: Wia.h
req.redist: 
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
tech.root: 
req.typenames: WIAVIDEO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaDevMgr.RegisterEventCallbackInterface
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
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

Specifies the event for which the application is registering. For a list of standard events, see <a href="https://msdn.microsoft.com/b94221b3-7cab-40d7-850a-fcc4ec8174b5">WIA Event Identifiers</a>.


### -param pIWiaEventCallback [in]

Type: <b><a href="https://msdn.microsoft.com/c5d82e08-51e6-4ee1-bb19-5030edefd5ce">IWiaEventCallback</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/c5d82e08-51e6-4ee1-bb19-5030edefd5ce">IWiaEventCallback</a> interface that the WIA system used to send the event notification.


### -param pEventObject [out]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

Receives the address of a pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Warning</b>  Using the <b>IWiaDevMgr::RegisterEventCallbackInterface</b>, <a href="https://msdn.microsoft.com/978dcd41-d63b-421d-b7e1-8e9368b36180">IWiaDevMgr2::RegisterEventCallbackInterface</a>, and <a href="https://msdn.microsoft.com/7186244e-0387-4206-8a9e-f379e566827e">DeviceManager.RegisterEvent</a> methods from the same process after the Still Image Service is restarted may cause an access violation, if the functions were used before the service was stopped.</div>
<div> </div>
When they begin executing, WIA applications use this method to register to receive hardware device events of the type WIA_NOTIFICATION_EVENT. This prevents the application from being restarted when another event for which it is registered occurs. Once a program invokes <b>IWiaDevMgr::RegisterEventCallbackInterface</b> to register itself to receive WIA events from a device, the registered events are routed to the program by the WIA system. 

Applications use the <a href="https://msdn.microsoft.com/fb35f225-3831-4442-b1e7-6314f59d158a">EnumRegisterEventInfo</a> method to retrieve a pointer to an enumerator object for event registration properties.

An application can find whether an event is an action type or notification type (or both) event by examinging the <b>ulFlags</b> value of a <a href="https://msdn.microsoft.com/9bf123c7-234f-45d3-bb45-c0cb135ef970">WIA_DEV_CAP</a> structure returned by event enumeration.

Applications can unregister for events by using the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer returned through the <i>pEventObject</i>  parameter to call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method.

<div class="alert"><b>Note</b>  In a multi-threaded application, there is no guarantee that the event notification callback will come in on the same thread that registered the callback.</div>
<div> </div>



---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWiaEventCallback::ImageEventCallback


## -description


The <b>IWiaEventCallback::ImageEventCallback</b> method is invoked by the Windows Image Acquisition (WIA) run-time system when a hardware device event occurs.


## -parameters




### -param pEventGUID [in]

Type: <b>const GUID*</b>

Specifies the unique identifier of the event. For a complete list of device events, see <a href="https://msdn.microsoft.com/b94221b3-7cab-40d7-850a-fcc4ec8174b5">WIA Event Identifiers</a>.


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

Specifies the type of the device. See <a href="https://msdn.microsoft.com/569b99ab-628b-4a43-a6e5-0ae81524fcc0">WIA Device Type Specifiers</a> for a list of possible values.


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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To receive notification of WIA hardware device events, applications pass a pointer to the <a href="https://msdn.microsoft.com/c5d82e08-51e6-4ee1-bb19-5030edefd5ce">IWiaEventCallback</a> interface to the <a href="https://msdn.microsoft.com/81a5bb61-5ec6-4c0b-8627-faccaf54d05a">RegisterEventCallbackInterface</a> method. The WIA run-time system then uses that interface pointer to invoke the <b>IWiaEventCallback::ImageEventCallback</b> method whenever a WIA hardware device event occurs.

Note that there is no guarantee the callback will be invoked on the same thread that registered the <a href="https://msdn.microsoft.com/c5d82e08-51e6-4ee1-bb19-5030edefd5ce">IWiaEventCallback</a> interface.




---
UID: NF:wmp.IWMPEvents2.DeviceStatusChange
title: IWMPEvents2::DeviceStatusChange (wmp.h)
description: The DeviceStatusChange event occurs when the partnership status of a device changes.
helpviewer_keywords: ["DeviceStatusChange","DeviceStatusChange method [Windows Media Player]","DeviceStatusChange method [Windows Media Player]","IWMPEvents2 interface","IWMPEvents2 interface [Windows Media Player]","DeviceStatusChange method","IWMPEvents2.DeviceStatusChange","IWMPEvents2::DeviceStatusChange","IWMPEvents2DeviceStatusChange","wmp.iwmpevents2_iwmpevents2__devicestatuschange","wmp/IWMPEvents2::DeviceStatusChange"]
old-location: wmp\iwmpevents2_iwmpevents2__devicestatuschange.htm
tech.root: WMP
ms.assetid: f9781dde-e813-4e2d-820d-5a0803bfbe4e
ms.date: 12/05/2018
ms.keywords: DeviceStatusChange, DeviceStatusChange method [Windows Media Player], DeviceStatusChange method [Windows Media Player],IWMPEvents2 interface, IWMPEvents2 interface [Windows Media Player],DeviceStatusChange method, IWMPEvents2.DeviceStatusChange, IWMPEvents2::DeviceStatusChange, IWMPEvents2DeviceStatusChange, wmp.iwmpevents2_iwmpevents2__devicestatuschange, wmp/IWMPEvents2::DeviceStatusChange
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEvents2::DeviceStatusChange
 - wmp/IWMPEvents2::DeviceStatusChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents2.DeviceStatusChange
---

# IWMPEvents2::DeviceStatusChange


## -description

The <b>DeviceStatusChange</b> event occurs when the partnership status of a device changes.

## -parameters

### -param pDevice [in]

Address of the <b>IWMPSyncDevice</b> interface that represents the device for which the status changed.

### -param NewStatus [in]

<b>WMPDeviceStatus</b> enumeration value that represents the new status for the device specified by <i>pDevice</i>.

## -remarks

Use <b>IWMPSyncDevice::isIdentical</b> to determine whether a particular device matches the device for which the status changed.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents2">IWMPEvents2 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical">IWMPSyncDevice::isIdentical</a>



<a href="/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus">WMPDeviceStatus</a>



<a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>
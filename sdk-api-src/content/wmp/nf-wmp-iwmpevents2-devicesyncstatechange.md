---
UID: NF:wmp.IWMPEvents2.DeviceSyncStateChange
title: IWMPEvents2::DeviceSyncStateChange (wmp.h)
description: The DeviceSyncStateChange event occurs when the synchronization state of a device changes.
helpviewer_keywords: ["DeviceSyncStateChange","DeviceSyncStateChange method [Windows Media Player]","DeviceSyncStateChange method [Windows Media Player]","IWMPEvents2 interface","IWMPEvents2 interface [Windows Media Player]","DeviceSyncStateChange method","IWMPEvents2.DeviceSyncStateChange","IWMPEvents2::DeviceSyncStateChange","IWMPEvents2DeviceSyncStateChange","wmp.iwmpevents2_iwmpevents2__devicesyncstatechange","wmp/IWMPEvents2::DeviceSyncStateChange"]
old-location: wmp\iwmpevents2_iwmpevents2__devicesyncstatechange.htm
tech.root: WMP
ms.assetid: 98970d33-8035-49f9-9243-b4832df6e5c9
ms.date: 12/05/2018
ms.keywords: DeviceSyncStateChange, DeviceSyncStateChange method [Windows Media Player], DeviceSyncStateChange method [Windows Media Player],IWMPEvents2 interface, IWMPEvents2 interface [Windows Media Player],DeviceSyncStateChange method, IWMPEvents2.DeviceSyncStateChange, IWMPEvents2::DeviceSyncStateChange, IWMPEvents2DeviceSyncStateChange, wmp.iwmpevents2_iwmpevents2__devicesyncstatechange, wmp/IWMPEvents2::DeviceSyncStateChange
f1_keywords:
- wmp/IWMPEvents2.DeviceSyncStateChange
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPEvents2.DeviceSyncStateChange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPEvents2::DeviceSyncStateChange


## -description



The <b>DeviceSyncStateChange</b> event occurs when the synchronization state of a device changes.




## -parameters




### -param pDevice [in]

Address of the <b>IWMPSyncDevice</b> interface that represents the device for which the synchronization state changed.


### -param NewState [in]

<b>WMPSyncState</b> enumeration value that represents the new synchronization state for the device specified by <i>pDevice</i>.


## -remarks



Use <b>IWMPSyncDevice::isIdentical</b> to determine whether a particular device matches the device for which the synchronization state changed.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpevents2">IWMPEvents2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical">IWMPSyncDevice::isIdentical</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/ne-wmp-wmpsyncstate">WMPSyncState</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>
 

 


---
UID: NF:wmp.IWMPEvents2.DeviceSyncError
title: IWMPEvents2::DeviceSyncError
author: windows-sdk-content
description: The DeviceSyncError event occurs in response to a synchronization error.
old-location: wmp\iwmpevents2_iwmpevents2__devicesyncerror.htm
tech.root: WMP
ms.assetid: 41e9a6df-3721-4fd2-aa9d-9874a004aa9a
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DeviceSyncError, DeviceSyncError method [Windows Media Player], DeviceSyncError method [Windows Media Player],IWMPEvents2 interface, IWMPEvents2 interface [Windows Media Player],DeviceSyncError method, IWMPEvents2.DeviceSyncError, IWMPEvents2::DeviceSyncError, IWMPEvents2DeviceSyncError, wmp.iwmpevents2_iwmpevents2__devicesyncerror, wmp/IWMPEvents2::DeviceSyncError
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IWMPEvents2.DeviceSyncError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents2::DeviceSyncError


## -description



The <b>DeviceSyncError</b> event occurs in response to a synchronization error.




## -parameters




### -param pDevice [in]

Address of the <b>IWMPSyncDevice</b> interface that represents the device for which the synchronization error occurred.


### -param pMedia [in]

Address of the <b>IWMPDispatch</b> interface that represents the media item for which the synchronization error occurred.


## -returns



This method does not return a value.




## -remarks



You should call <b>QueryInterface</b> on <i>pMedia</i> to get the <b>IWMPMedia2</b> interface for the <b>Media</b> object. You can then use <b>IWMPMedia2::get_error</b> to retrieve more information about the error that occurred.

Use <b>IWMPSyncDevice::isIdentical</b> to determine whether a particular device matches the device for which the error occurred.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/61cd0a2e-b94f-4c10-b3e2-ad1dc2a0b17d">IWMPEvents2 Interface</a>



<a href="https://msdn.microsoft.com/e5d1e4f8-4a31-427e-ac2e-e7d4c3194a21">IWMPMedia2 Interface</a>



<a href="https://msdn.microsoft.com/4335d480-5af0-4764-b8f8-0e6edc1598b7">IWMPSyncDevice::isIdentical</a>



<a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents Interface</a>
 

 


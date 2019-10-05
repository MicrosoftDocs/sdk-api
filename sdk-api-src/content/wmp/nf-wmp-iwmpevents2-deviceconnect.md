---
UID: NF:wmp.IWMPEvents2.DeviceConnect
title: IWMPEvents2::DeviceConnect (wmp.h)
author: windows-sdk-content
description: The DeviceConnect event occurs when the user connects a device to the computer.
old-location: wmp\iwmpevents2_iwmpevents2__deviceconnect.htm
tech.root: WMP
ms.assetid: ed726579-e0cb-4007-98eb-b6df4b636b12
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeviceConnect, DeviceConnect method [Windows Media Player], DeviceConnect method [Windows Media Player],IWMPEvents2 interface, IWMPEvents2 interface [Windows Media Player],DeviceConnect method, IWMPEvents2.DeviceConnect, IWMPEvents2::DeviceConnect, IWMPEvents2DeviceConnect, wmp.iwmpevents2_iwmpevents2__deviceconnect, wmp/IWMPEvents2::DeviceConnect
ms.topic: method
f1_keywords: 
 - "wmp/IWMPEvents2.DeviceConnect"
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
 - IWMPEvents2.DeviceConnect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPEvents2::DeviceConnect


## -description



The <b>DeviceConnect</b> event occurs when the user connects a device to the computer.




## -parameters




### -param pDevice [in]

Address of the <b>IWMPSyncDevice</b> interface that represents the device that the user connected.


## -returns



This method does not return a value.




## -remarks



You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpevents2">IWMPEvents2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical">IWMPSyncDevice::isIdentical</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>
 

 


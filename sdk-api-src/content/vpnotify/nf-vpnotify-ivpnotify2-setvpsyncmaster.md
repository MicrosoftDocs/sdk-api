---
UID: NF:vpnotify.IVPNotify2.SetVPSyncMaster
title: IVPNotify2::SetVPSyncMaster
author: windows-sdk-content
description: The SetVPSyncMaster method sets whether the video port controls vertical synchronization of the VGA.
old-location: dshow\ivpnotify2_setvpsyncmaster.htm
old-project: DirectShow
ms.assetid: ef1075a6-f31b-4ad8-b31a-66ca68d2c068
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IVPNotify2 interface [DirectShow],SetVPSyncMaster method, IVPNotify2.SetVPSyncMaster, IVPNotify2::SetVPSyncMaster, IVPNotify2SetVPSyncMaster, SetVPSyncMaster, SetVPSyncMaster method [DirectShow], SetVPSyncMaster method [DirectShow],IVPNotify2 interface, dshow.ivpnotify2_setvpsyncmaster, vpnotify/IVPNotify2::SetVPSyncMaster
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vpnotify.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: VMR9VideoStreamInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVPNotify2.SetVPSyncMaster
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVPNotify2::SetVPSyncMaster


## -description



The <code>SetVPSyncMaster</code> method sets whether the video port controls vertical synchronization of the VGA.




## -parameters




### -param bVPSyncMaster [in]

Value specifying whether the video port controls the vertical synchronization of the VGA monitor. <b>TRUE</b> if the port controls the monitor's synchronization; <b>FALSE</b> otherwise.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Include Vptype.h before Vpnotify.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8d5fc7ee-93ee-4297-ba24-0eed63bec1ea">IVPNotify2 Interface</a>
 

 


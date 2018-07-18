---
UID: NF:vpnotify.IVPNotify2.GetVPSyncMaster
title: IVPNotify2::GetVPSyncMaster
author: windows-sdk-content
description: The GetVPSyncMaster method checks whether the video port controls the synchronization of the VGA.
old-location: dshow\ivpnotify2_getvpsyncmaster.htm
old-project: DirectShow
ms.assetid: afc75615-1be5-4f1f-ace2-f3a17420b591
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetVPSyncMaster, GetVPSyncMaster method [DirectShow], GetVPSyncMaster method [DirectShow],IVPNotify2 interface, IVPNotify2 interface [DirectShow],GetVPSyncMaster method, IVPNotify2.GetVPSyncMaster, IVPNotify2::GetVPSyncMaster, IVPNotify2GetVPSyncMaster, dshow.ivpnotify2_getvpsyncmaster, vpnotify/IVPNotify2::GetVPSyncMaster
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vpnotify.h
req.include-header: 
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
 - IVPNotify2.GetVPSyncMaster
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVPNotify2::GetVPSyncMaster


## -description



The <code>GetVPSyncMaster</code> method checks whether the video port controls the synchronization of the VGA.




## -parameters




### -param pbVPSyncMaster [out]

Pointer to a value indicating whether the video port controls the vertical synchronization of the VGA monitor. <b>TRUE</b> if the port controls the monitor's synchronization; <b>FALSE</b> otherwise.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Include Vptype.h before Vpnotify.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8d5fc7ee-93ee-4297-ba24-0eed63bec1ea">IVPNotify2 Interface</a>
 

 


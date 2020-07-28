---
UID: NF:vpnotify.IVPNotify2.SetVPSyncMaster
title: IVPNotify2::SetVPSyncMaster (vpnotify.h)
description: The SetVPSyncMaster method sets whether the video port controls vertical synchronization of the VGA.
helpviewer_keywords: ["IVPNotify2 interface [DirectShow]","SetVPSyncMaster method","IVPNotify2.SetVPSyncMaster","IVPNotify2::SetVPSyncMaster","IVPNotify2SetVPSyncMaster","SetVPSyncMaster","SetVPSyncMaster method [DirectShow]","SetVPSyncMaster method [DirectShow]","IVPNotify2 interface","dshow.ivpnotify2_setvpsyncmaster","vpnotify/IVPNotify2::SetVPSyncMaster"]
old-location: dshow\ivpnotify2_setvpsyncmaster.htm
tech.root: dshow
ms.assetid: ef1075a6-f31b-4ad8-b31a-66ca68d2c068
ms.date: 12/05/2018
ms.keywords: IVPNotify2 interface [DirectShow],SetVPSyncMaster method, IVPNotify2.SetVPSyncMaster, IVPNotify2::SetVPSyncMaster, IVPNotify2SetVPSyncMaster, SetVPSyncMaster, SetVPSyncMaster method [DirectShow], SetVPSyncMaster method [DirectShow],IVPNotify2 interface, dshow.ivpnotify2_setvpsyncmaster, vpnotify/IVPNotify2::SetVPSyncMaster
f1_keywords:
- vpnotify/IVPNotify2.SetVPSyncMaster
dev_langs:
- c++
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2">IVPNotify2 Interface</a>
 

 


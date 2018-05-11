---
UID: NF:vpnotify.IVPNotify.GetDeinterlaceMode
title: IVPNotify::GetDeinterlaceMode
author: windows-driver-content
description: The GetDeinterlaceMode method retrieves the mode (such as bob or weave).
old-location: dshow\ivpnotify_getdeinterlacemode.htm
old-project: DirectShow
ms.assetid: 08d28857-5460-407d-a169-8568b2c381e6
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetDeinterlaceMode, GetDeinterlaceMode method [DirectShow], GetDeinterlaceMode method [DirectShow],IVPNotify interface, IVPNotify interface [DirectShow],GetDeinterlaceMode method, IVPNotify.GetDeinterlaceMode, IVPNotify::GetDeinterlaceMode, IVPNotifyGetDeinterlaceMode, dshow.ivpnotify_getdeinterlacemode, vpnotify/IVPNotify::GetDeinterlaceMode
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: VMR9VideoStreamInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVPNotify.GetDeinterlaceMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVPNotify::GetDeinterlaceMode


## -description



The <code>GetDeinterlaceMode</code> method retrieves the mode (such as bob or weave).



This method is not currently implemented and returns E_NOTIMPL.


## -parameters




### -param pMode






#### - pmode [out]

Pointer to the retrieved mode. This value is a member of the <a href="https://msdn.microsoft.com/73d63ca2-17fb-4e27-9ea5-62686117254a">AMVP_MODE</a> enumerated data type.


## -returns



Returns E_NOTIMPL.




## -remarks



Include Vptype.h before Vpnotify.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b40ba9e-8562-4d31-beaf-e4d4858bf145">IVPNotify Interface</a>
 

 


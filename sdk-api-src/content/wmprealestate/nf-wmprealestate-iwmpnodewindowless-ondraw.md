---
UID: NF:wmprealestate.IWMPNodeWindowless.OnDraw
title: IWMPNodeWindowless::OnDraw
author: windows-driver-content
description: This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
old-location: wmp\iwmpnodewindowless_ondraw.htm
old-project: WMP
ms.assetid: 2691cce8-590c-4604-9607-16f6e0799618
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: IWMPNodeWindowless interface [Windows Media Player],OnDraw method, IWMPNodeWindowless.OnDraw, IWMPNodeWindowless::OnDraw, IWMPNodeWindowlessOnDrawRendering, OnDraw, OnDraw method [Windows Media Player], OnDraw method [Windows Media Player],IWMPNodeWindowless interface, wmp.iwmpnodewindowless_ondraw, wmprealestate/IWMPNodeWindowless::OnDraw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmprealestate.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.typenames: WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmprealestate.h
api_name:
-	IWMPNodeWindowless.OnDraw
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNodeWindowless::OnDraw


## -description




          This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
        



The <b>OnDraw</b> method receives a handle to a device context and a <b>RECT</b> structure for drawing in windowless mode.


## -parameters




### -param hdc [in]

A handle to a device context.


### -param prcDraw [in]

A <b>RECT</b> structure representing the drawing area.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



This is the method that initiates rendering when in windowless mode.




## -see-also




<a href="https://msdn.microsoft.com/585f59cc-e074-4196-a851-d1e3ff9a4500">IWMPNodeWindowless Interface (deprecated)</a>
 

 


---
UID: NF:wmprealestate.IWMPNodeRealEstate.SetFullScreen
title: IWMPNodeRealEstate::SetFullScreen
author: windows-driver-content
description: This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
old-location: wmp\iwmpnoderealestate_setfullscreen.htm
old-project: WMP
ms.assetid: 63d3363d-3104-4760-b185-fd75547a53ec
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: IWMPNodeRealEstate interface [Windows Media Player],SetFullScreen method, IWMPNodeRealEstate.SetFullScreen, IWMPNodeRealEstate::SetFullScreen, IWMPNodeRealEstateSetFullScreenRendering, SetFullScreen, SetFullScreen method [Windows Media Player], SetFullScreen method [Windows Media Player],IWMPNodeRealEstate interface, wmp.iwmpnoderealestate_setfullscreen, wmprealestate/IWMPNodeRealEstate::SetFullScreen
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
-	IWMPNodeRealEstate.SetFullScreen
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNodeRealEstate::SetFullScreen


## -description




          This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
        



The <b>SetFullScreen</b> method receives a value indicating that Windows Media Player is switching to full screen mode.


## -parameters




### -param fFullScreen [in]

<b>Boolean</b>, true indicating full screen.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



Use this method to initialize any code related to full screen rendering. Do not use this method as a cue to begin rendering.




## -see-also




<a href="https://msdn.microsoft.com/0c9d382a-26de-4e53-9950-76916863f116">IWMPNodeRealEstate Interface (deprecated)</a>



<a href="https://msdn.microsoft.com/70e028be-c824-4e6d-858d-be1c4a4ea670">IWMPNodeRealEstate::GetFullScreen (deprecated)</a>
 

 


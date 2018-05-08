---
UID: NF:wmprealestate.IWMPNodeRealEstate.GetFullScreen
title: IWMPNodeRealEstate::GetFullScreen
author: windows-driver-content
description: This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
old-location: wmp\iwmpnoderealestate_getfullscreen.htm
old-project: WMP
ms.assetid: 70e028be-c824-4e6d-858d-be1c4a4ea670
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: GetFullScreen, GetFullScreen method [Windows Media Player], GetFullScreen method [Windows Media Player],IWMPNodeRealEstate interface, IWMPNodeRealEstate interface [Windows Media Player],GetFullScreen method, IWMPNodeRealEstate.GetFullScreen, IWMPNodeRealEstate::GetFullScreen, IWMPNodeRealEstateGetFullScreenRendering, wmp.iwmpnoderealestate_getfullscreen, wmprealestate/IWMPNodeRealEstate::GetFullScreen
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
-	IWMPNodeRealEstate.GetFullScreen
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNodeRealEstate::GetFullScreen


## -description




          This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
        



The <b>GetFullScreen</b> method returns a value indicating the current rendering state of the Player.


## -parameters




### -param pfFullScreen [out]

Pointer to a <b>Boolean</b>, <b>true</b> indicating full screen.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



If <b>TRUE</b>, the Player is currently in full screen mode. If <b>FALSE</b>, the Player is currently displaying in full mode or skin mode.




## -see-also




<a href="https://msdn.microsoft.com/0c9d382a-26de-4e53-9950-76916863f116">IWMPNodeRealEstate Interface (deprecated)</a>



<a href="https://msdn.microsoft.com/63d3363d-3104-4760-b185-fd75547a53ec">IWMPNodeRealEstate::SetFullScreen (deprecated)</a>
 

 


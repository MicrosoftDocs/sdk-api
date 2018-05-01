---
UID: NF:wmprealestate.IWMPNodeRealEstateHost.OnFullScreenTransition
title: IWMPNodeRealEstateHost::OnFullScreenTransition method
author: windows-driver-content
description: This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
old-location: wmp\iwmpnoderealestatehost_onfullscreentransition.htm
old-project: WMP
ms.assetid: 0519dc05-7517-4ea4-9940-757bfa6296ff
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPNodeRealEstateHost, IWMPNodeRealEstateHost interface [Windows Media Player], OnFullScreenTransition method, IWMPNodeRealEstateHost::OnFullScreenTransition, IWMPNodeRealEstateHostOnFullScreenTransitionRendering, OnFullScreenTransition method [Windows Media Player], OnFullScreenTransition method [Windows Media Player], IWMPNodeRealEstateHost interface, OnFullScreenTransition,IWMPNodeRealEstateHost.OnFullScreenTransition, wmp.iwmpnoderealestatehost_onfullscreentransition, wmprealestate/IWMPNodeRealEstateHost::OnFullScreenTransition
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
-	wmp.dll
api_name:
-	IWMPNodeRealEstateHost.OnFullScreenTransition
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNodeRealEstateHost::OnFullScreenTransition method


## -description




          This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
        



The <b>OnFullScreenTransition</b> method requests a transition to full screen rendering.


## -parameters




### -param fFullScreen [in]

<b>Boolean</b>, true indicating full screen.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



When the Player transitions to full screen mode, it calls <b>IWMPNodeRealEstate::SetFullScreen</b>.




## -see-also




<a href="https://msdn.microsoft.com/63d3363d-3104-4760-b185-fd75547a53ec">IWMPNodeRealEstate::SetFullScreen (deprecated)</a>



<a href="https://msdn.microsoft.com/fb83007d-4844-4c05-ab79-f4a6bd62497e">IWMPNodeRealEstateHost Interface (deprecated)</a>
 

 


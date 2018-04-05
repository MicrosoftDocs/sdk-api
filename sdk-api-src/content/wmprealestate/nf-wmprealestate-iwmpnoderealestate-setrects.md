---
UID: NF:wmprealestate.IWMPNodeRealEstate.SetRects
title: IWMPNodeRealEstate::SetRects method
author: windows-driver-content
description: This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
old-location: wmp\iwmpnoderealestate_setrects.htm
old-project: WMP
ms.assetid: 0742cef9-192b-4680-83e5-350e7024a042
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPNodeRealEstate, IWMPNodeRealEstate interface [Windows Media Player], SetRects method, IWMPNodeRealEstate::SetRects, IWMPNodeRealEstateSetRectsRendering, SetRects method [Windows Media Player], SetRects method [Windows Media Player], IWMPNodeRealEstate interface, SetRects,IWMPNodeRealEstate.SetRects, wmp.iwmpnoderealestate_setrects, wmprealestate/IWMPNodeRealEstate::SetRects
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
-	IWMPNodeRealEstate.SetRects
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNodeRealEstate::SetRects method


## -description




          This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
        



The <b>SetRects</b> method receives information about the rendering area provided by Windows Media Player.


## -parameters




### -param pSrc [in]

Pointer to a <b>RECT</b> object that represents the portion of the original image that is to be rendered.


### -param pDest [in]

Pointer to a <b>RECT</b> object that represents stretching/shrinking of the original image as well as positioning relative to the origin of the owner window.


### -param pClip [in]

Pointer to a <b>RECT</b> object that represents the portion of the destination rectangle that should actually be visible to the user.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



Once the plug-in receives the <b>RECT</b> objects, it can immediately proceed with rendering.




## -see-also




<a href="https://msdn.microsoft.com/0c9d382a-26de-4e53-9950-76916863f116">IWMPNodeRealEstate Interface (deprecated)</a>



<a href="https://msdn.microsoft.com/2bb07fe6-67cd-46da-a012-0276e31e48c9">IWMPNodeRealEstate::GetRects (deprecated)</a>
 

 


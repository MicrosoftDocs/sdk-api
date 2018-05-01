---
UID: NF:wmprealestate.IWMPNodeRealEstate.GetRects
title: IWMPNodeRealEstate::GetRects method
author: windows-driver-content
description: This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
old-location: wmp\iwmpnoderealestate_getrects.htm
old-project: WMP
ms.assetid: 2bb07fe6-67cd-46da-a012-0276e31e48c9
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: GetRects method [Windows Media Player], GetRects method [Windows Media Player], IWMPNodeRealEstate interface, GetRects,IWMPNodeRealEstate.GetRects, IWMPNodeRealEstate, IWMPNodeRealEstate interface [Windows Media Player], GetRects method, IWMPNodeRealEstate::GetRects, IWMPNodeRealEstateGetRectsRendering, wmp.iwmpnoderealestate_getrects, wmprealestate/IWMPNodeRealEstate::GetRects
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
-	IWMPNodeRealEstate.GetRects
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNodeRealEstate::GetRects method


## -description




          This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
        



The <b>GetRects</b> method returns the three <b>RECT</b> structures previously set in the plug-in.


## -parameters




### -param pSrc [out]

Pointer to a <b>RECT</b> object that represents the portion of the original image that is to be rendered.


### -param pDest [out]

Pointer to a <b>RECT</b> object that represents stretching/shrinking of the original image as well as positioning relative to the origin of the owner window.


### -param pClip [out]

Pointer to a <b>RECT</b> object that represents the portion of the destination rectangle that should actually be visible to the user.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



Any of these values can be set to <b>NULL</b>. The plug-in must not change values returned by this method.




## -see-also




<a href="https://msdn.microsoft.com/0c9d382a-26de-4e53-9950-76916863f116">IWMPNodeRealEstate Interface (deprecated)</a>



<a href="https://msdn.microsoft.com/0742cef9-192b-4680-83e5-350e7024a042">IWMPNodeRealEstate::SetRects (deprecated)</a>
 

 


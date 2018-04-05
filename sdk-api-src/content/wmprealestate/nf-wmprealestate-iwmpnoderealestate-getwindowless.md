---
UID: NF:wmprealestate.IWMPNodeRealEstate.GetWindowless
title: IWMPNodeRealEstate::GetWindowless method
author: windows-driver-content
description: This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
old-location: wmp\iwmpnoderealestate_getwindowless.htm
old-project: WMP
ms.assetid: 6a45969c-5eba-4493-a7a8-af69f5ad3dea
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetWindowless method [Windows Media Player], GetWindowless method [Windows Media Player], IWMPNodeRealEstate interface, GetWindowless,IWMPNodeRealEstate.GetWindowless, IWMPNodeRealEstate, IWMPNodeRealEstate interface [Windows Media Player], GetWindowless method, IWMPNodeRealEstate::GetWindowless, IWMPNodeRealEstateGetWindowlessRendering, wmp.iwmpnoderealestate_getwindowless, wmprealestate/IWMPNodeRealEstate::GetWindowless
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
-	IWMPNodeRealEstate.GetWindowless
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNodeRealEstate::GetWindowless method


## -description




          This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
        



The <b>GetWindowless</b> method returns a value indicating whether the plug-in is currently rendering in windowless mode.


## -parameters




### -param pfWindowless [out]

Pointer to a <b>Boolean</b>, true indicating windowless.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



Do not change values returned by this method.




## -see-also




<a href="https://msdn.microsoft.com/0c9d382a-26de-4e53-9950-76916863f116">IWMPNodeRealEstate Interface (deprecated)</a>



<a href="https://msdn.microsoft.com/408d33f6-916f-4443-8a92-fab00c11cad4">IWMPNodeRealEstate::SetWindowless (deprecated)</a>
 

 


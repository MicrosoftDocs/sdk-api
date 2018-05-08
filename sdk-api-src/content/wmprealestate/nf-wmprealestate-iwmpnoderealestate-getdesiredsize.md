---
UID: NF:wmprealestate.IWMPNodeRealEstate.GetDesiredSize
title: IWMPNodeRealEstate::GetDesiredSize
author: windows-driver-content
description: This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
old-location: wmp\iwmpnoderealestate_getdesiredsize.htm
old-project: WMP
ms.assetid: 41a7edf3-10a3-41ac-8f79-6dc0e7f854ee
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: GetDesiredSize, GetDesiredSize method [Windows Media Player], GetDesiredSize method [Windows Media Player],IWMPNodeRealEstate interface, IWMPNodeRealEstate interface [Windows Media Player],GetDesiredSize method, IWMPNodeRealEstate.GetDesiredSize, IWMPNodeRealEstate::GetDesiredSize, IWMPNodeRealEstateGetDesiredSizeRendering, wmp.iwmpnoderealestate_getdesiredsize, wmprealestate/IWMPNodeRealEstate::GetDesiredSize
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
-	IWMPNodeRealEstate.GetDesiredSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNodeRealEstate::GetDesiredSize


## -description




          This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
        



The <b>GetDesiredSize</b> method returns the size of the rendering area requested by the plug-in.


## -parameters




### -param pSize [out]

A long pointer to a <b>SIZE</b> structure.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



The <b>SIZE</b> structure stores width and height as x and y coordinates. For more information about the <b>SIZE</b> structure, see the Platform SDK.




## -see-also




<a href="https://msdn.microsoft.com/0c9d382a-26de-4e53-9950-76916863f116">IWMPNodeRealEstate Interface (deprecated)</a>
 

 


---
UID: NF:wmprealestate.IWMPNodeWindowlessHost.InvalidateRect
title: IWMPNodeWindowlessHost::InvalidateRect
author: windows-driver-content
description: This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
old-location: wmp\iwmpnodewindowlesshost_invalidaterect.htm
old-project: WMP
ms.assetid: 35fdb7cb-d885-4c01-998a-dab16b301bd4
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: IWMPNodeWindowlessHost interface [Windows Media Player],InvalidateRect method, IWMPNodeWindowlessHost.InvalidateRect, IWMPNodeWindowlessHost::InvalidateRect, IWMPNodeWindowlessHostInvalidateRectRendering, InvalidateRect, InvalidateRect method [Windows Media Player], InvalidateRect method [Windows Media Player],IWMPNodeWindowlessHost interface, wmp.iwmpnodewindowlesshost_invalidaterect, wmprealestate/IWMPNodeWindowlessHost::InvalidateRect
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
-	IWMPNodeWindowlessHost.InvalidateRect
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNodeWindowlessHost::InvalidateRect


## -description




          This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
        



The <b>InvalidateRect</b> method directs Windows Media Player to refresh the windowless display area.


## -parameters




### -param prc [in]

Specifies the region to update.


### -param fErase [in]

Flag, true indicating erase.


## -returns



The method returns an <b>HRESULT</b>.




## -see-also




<a href="https://msdn.microsoft.com/b0bcf5d3-9f12-498b-b085-49e206b0b49b">IWMPNodeWindowlessHost Interface (deprecated)</a>
 

 


---
UID: NF:wmprealestate.IWMPNodeRealEstateHost.OnDesiredSizeChange
title: IWMPNodeRealEstateHost::OnDesiredSizeChange
author: windows-driver-content
description: This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
old-location: wmp\iwmpnoderealestatehost_ondesiredsizechange.htm
old-project: WMP
ms.assetid: 339bfed3-8688-4474-a280-f1b0a5a5c597
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: IWMPNodeRealEstateHost interface [Windows Media Player],OnDesiredSizeChange method, IWMPNodeRealEstateHost.OnDesiredSizeChange, IWMPNodeRealEstateHost::OnDesiredSizeChange, IWMPNodeRealEstateHostOnDesiredSizeChangeRendering, OnDesiredSizeChange, OnDesiredSizeChange method [Windows Media Player], OnDesiredSizeChange method [Windows Media Player],IWMPNodeRealEstateHost interface, wmp.iwmpnoderealestatehost_ondesiredsizechange, wmprealestate/IWMPNodeRealEstateHost::OnDesiredSizeChange
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
-	IWMPNodeRealEstateHost.OnDesiredSizeChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNodeRealEstateHost::OnDesiredSizeChange


## -description




          This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
        



The <b>OnDesiredSizeChange</b> method requests a size change from Windows Media Player.


## -parameters




### -param pSize [in]

Pointer to a <b>SIZE</b> structure that represents the desired size as x,y coordinates.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



A call to this method is not a guarantee that the rendering size has actually changed. Actual rendering information is always conveyed by <b>IWMPNodeRealEstate::SetRects</b>.

For more information about the <b>SIZE</b> structure, see the Platform SDK.




## -see-also




<a href="https://msdn.microsoft.com/0742cef9-192b-4680-83e5-350e7024a042">IWMPNodeRealEstate::SetRects (deprecated)</a>



<a href="https://msdn.microsoft.com/fb83007d-4844-4c05-ab79-f4a6bd62497e">IWMPNodeRealEstateHost Interface (deprecated)</a>
 

 


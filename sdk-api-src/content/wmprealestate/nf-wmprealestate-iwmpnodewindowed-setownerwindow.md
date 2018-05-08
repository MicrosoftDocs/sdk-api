---
UID: NF:wmprealestate.IWMPNodeWindowed.SetOwnerWindow
title: IWMPNodeWindowed::SetOwnerWindow
author: windows-driver-content
description: This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
old-location: wmp\iwmpnodewindowed_setownerwindow.htm
old-project: WMP
ms.assetid: 33541e65-57dc-488a-ab34-6ac2e5ecda58
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: IWMPNodeWindowed interface [Windows Media Player],SetOwnerWindow method, IWMPNodeWindowed.SetOwnerWindow, IWMPNodeWindowed::SetOwnerWindow, IWMPNodeWindowedSetOwnerWindowRendering, SetOwnerWindow, SetOwnerWindow method [Windows Media Player], SetOwnerWindow method [Windows Media Player],IWMPNodeWindowed interface, wmp.iwmpnodewindowed_setownerwindow, wmprealestate/IWMPNodeWindowed::SetOwnerWindow
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
-	IWMPNodeWindowed.SetOwnerWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNodeWindowed::SetOwnerWindow


## -description




          This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.
        



The <b>SetOwnerWindow</b> method receives a handle to a parent window. The plug-in can use this parent window to derive a child window for rendering.


## -parameters




### -param hwnd [in]

A handle to the window to be used for rendering.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



Rendering in a child window gives you the advantage of keeping the RECT coordinates returned from the Player consistent when the parent window position changes. Coordinate values will remain relative to the parent window, as opposed to relative to the Windows desktop.




## -see-also




<a href="https://msdn.microsoft.com/ef99ff7c-d4b0-448e-8057-037535aaf847">IWMPNodeWindowed Interface (deprecated)</a>



<a href="https://msdn.microsoft.com/d42bdb97-6821-4e4a-b98d-ed03f978b5c1">IWMPNodeWindowed::GetOwnerWindow (deprecated)</a>
 

 


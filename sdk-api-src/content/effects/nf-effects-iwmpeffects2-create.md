---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# IWMPEffects2::Create


## -description



The <b>Create</b> method is called by Windows Media Player to instantiate a visualization window.




## -parameters




### -param hwndParent [in]

<b>HWND</b> handle to the parent window hosting the visualization window.


## -returns



This method returns an <b>HRESULT</b>.




## -remarks



A visualization that implements <b>IWMPEffects2</b> is rendered in its own window unless it will be displayed in a clipped device context, in which case it is rendered windowless. For a visualization that is rendered windowless, Windows Media Player calls this method with a <b>NULL</b> value for the <i>hwndParent</i> parameter. If your visualization does not support windowless mode (for example, when using Direct3D), it should return a failure <b>HRESULT</b> value. In this case, your visualization will not be available in skins that clip the display region.

If you create a visualization for Windows Media Player using the Direct3D® component of Microsoft DirectX®, you must set the <b>D3DCREATE_FPU_PRESERVE</b> flag when calling <b>IDirect3D8::CreateDevice</b>. Failure to set this flag for visualizations that use Direct3D may yield unexpected results.




## -see-also




<a href="https://msdn.microsoft.com/44e044c1-97fd-43cb-9530-4556e485f5ae">IWMPEffects2 Interface</a>



<a href="https://msdn.microsoft.com/dad290e6-a3be-47f0-a893-7a60eebc2a64">IWMPEffects2::Destroy</a>
 

 


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

# IOverlay::SetColorKey


## -description



The <code>SetColorKey</code> method changes the color key.




## -parameters




### -param pColorKey [in, out]

Pointer to the color key value to be set. If successful, the actual color key value selected is copied to this parameter.


## -returns



Returns S_OK if successful, E_POINTER if <i>pColorKey</i> is <b>NULL</b>, or E_INVALIDARG if the value of <i>pColorKey</i> is invalid for the current palette or pixel format.




## -remarks



If you change the color key using the <code>SetColorKey</code> method, all the advise links will receive an <a href="https://msdn.microsoft.com/a1e7fc88-a50a-4832-9b29-21b94184f1c7">IOverlayNotify::OnColorKeyChange</a> callback method with the new color.

When using <a href="https://msdn.microsoft.com/02db2233-b185-47a9-9655-409991a74d4e">IOverlay::Advise</a> on a palettized display, a filter can either install a color key (using <code>SetColorKey</code>) or install a palette (using <a href="https://msdn.microsoft.com/572f77ab-08a8-453a-993b-724da967bcde">IOverlay::SetPalette</a>), but not both. This is because color keys in this mode require a palette to be realized that would conflict with <b>SetPalette</b>. Color keys can be uninstalled by requesting a color key with the CK_NOCOLORKEY flag. Likewise, any palette installed through <b>SetPalette</b> can be uninstalled by calling <b>SetPalette</b> and passing in <b>NULL</b> parameters (that is, SetPalette(0,<b>NULL</b>)).

Trying to set a palette when a color key is installed returns a VFW_E_PALETTE_SET error. Trying to set a color key when a palette is installed returns VFW_E_COLOR_KEY_SET.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2d49888a-7046-4779-9634-d181fa582584">IOverlay Interface</a>
 

 


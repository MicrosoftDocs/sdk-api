---
UID: NF:ocidl.IFont.SetRatio
title: IFont::SetRatio
author: windows-sdk-content
description: Converts the scaling factor for this font between logical units and HIMETRIC units.
old-location: com\ifont_setratio.htm
tech.root: com
ms.assetid: aaa962d8-6f7f-4031-aa10-09cadf0e5aec
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IFont interface [COM],SetRatio method, IFont.SetRatio, IFont::SetRatio, SetRatio, SetRatio method [COM], SetRatio method [COM],IFont interface, _ctrl_ifont_setratio, com.ifont_setratio, ocidl/IFont::SetRatio
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IFont.SetRatio
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFont::SetRatio


## -description


Converts the scaling factor for this font between logical units and <b>HIMETRIC</b> units. 
    <b>HIMETRIC</b> units are used to express the point size in the 
    <a href="https://msdn.microsoft.com/aeee7dfc-5ccd-4c30-a59e-5eec93505288">IFont::get_Size</a> and 
    <a href="https://msdn.microsoft.com/1c39a7dc-553b-41b7-8b66-1a5980493dce">IFont::put_Size</a> methods. The values passed to 
    <b>IFont::SetRatio</b> are used to compute the display size of 
    the font in logical units from the value in the <b>Size</b> property:

<code>Display Size = ( cyLogical / cyHimetric ) * Size</code>


## -parameters




### -param cyLogical [in]

The font size, in logical units.


### -param cyHimetric [in]

The font size, in <b>HIMETRIC</b> units.


## -returns



The method supports the standard return values E_UNEXPECTED, E_INVALIDARG, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/aeee7dfc-5ccd-4c30-a59e-5eec93505288">IFont::get_Size</a>



<a href="https://msdn.microsoft.com/1c39a7dc-553b-41b7-8b66-1a5980493dce">IFont::put_Size</a>
 

 


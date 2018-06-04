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

# ITextFont2::GetPositionSubSuper


## -description


Gets the subscript or superscript position relative to the baseline.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The subscript or superscript position relative to the baseline.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The subscript or superscript position is relative to the baseline as a percent of the font height.

Subscripts and superscripts in math zones are handled using the <a href="objecttype.htm">tomSubscript</a>, <a href="objecttype.htm">tomSuperscript</a>, <a href="objecttype.htm">tomSubSup</a>, and <a href="objecttype.htm">tomLeftSubSup</a> mathematical objects. See <a href="https://msdn.microsoft.com/0ed4a595-c3e8-4bfa-805f-4c5dfd5e3a56">ITextRange2::GetInlineObject</a>.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/3f78a91b-17a3-48ff-9ca0-1eb4f9c95be4">ITextFont2::SetPositionSubSuper</a>
 

 


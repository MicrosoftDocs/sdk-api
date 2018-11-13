---
UID: NF:directmanipulation.IDirectManipulationContent.GetContentRect
title: IDirectManipulationContent::GetContentRect
author: windows-sdk-content
description: Retrieves the bounding rectangle of the content, relative to the bounding rectangle of the viewport (if defined).
old-location: directmanipulation\idirectmanipulationcontent_getcontentrect.htm
tech.root: directmanipulation
ms.assetid: 26a5736e-633e-4451-a339-c5f88913bcf6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetContentRect, GetContentRect method [Direct Manipulation], GetContentRect method [Direct Manipulation],IDirectManipulationContent interface, IDirectManipulationContent interface [Direct Manipulation],GetContentRect method, IDirectManipulationContent.GetContentRect, IDirectManipulationContent::GetContentRect, directmanipulation.idirectmanipulationcontent_getcontentrect, directmanipulation/IDirectManipulationContent::GetContentRect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
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
 - DirectManipulation.h
api_name:
 - IDirectManipulationContent.GetContentRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationContent::GetContentRect


## -description


Retrieves the bounding rectangle of the content, relative to the bounding rectangle of the viewport (if defined).


## -parameters




### -param contentSize [out]

The bounding rectangle of the content.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



If the bounding rectangle  has not been set using <a href="https://msdn.microsoft.com/41b14e56-ba24-4ad2-9dac-28daf7d13c6a">SetContentRect</a>, then <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">UI_E_VALUE_NOT_SET</a> is returned. However, the actual content rectangle is (-<a href="_pluslang_Floating_Limits">FLT_MAX</a>, -<a href="_pluslang_Floating_Limits">FLT_MAX</a>, <a href="_pluslang_Floating_Limits">FLT_MAX</a>, <a href="_pluslang_Floating_Limits">FLT_MAX</a>).




## -see-also




<a href="https://msdn.microsoft.com/4d69a503-f998-4197-824f-4df48825c941">IDirectManipulationContent</a>
 

 


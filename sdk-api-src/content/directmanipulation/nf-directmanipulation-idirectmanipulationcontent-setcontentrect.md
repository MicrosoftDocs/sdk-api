---
UID: NF:directmanipulation.IDirectManipulationContent.SetContentRect
title: IDirectManipulationContent::SetContentRect
author: windows-sdk-content
description: Specifies the bounding rectangle of the content, relative to its viewport.
old-location: directmanipulation\idirectmanipulationcontent_setcontentrect.htm
tech.root: directmanipulation
ms.assetid: 41b14e56-ba24-4ad2-9dac-28daf7d13c6a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectManipulationContent interface [Direct Manipulation],SetContentRect method, IDirectManipulationContent.SetContentRect, IDirectManipulationContent::SetContentRect, SetContentRect, SetContentRect method [Direct Manipulation], SetContentRect method [Direct Manipulation],IDirectManipulationContent interface, directmanipulation.idirectmanipulationcontent_setcontentrect, directmanipulation/IDirectManipulationContent::SetContentRect
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
 - IDirectManipulationContent.SetContentRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationContent::SetContentRect


## -description


Specifies the bounding rectangle of the content, relative to its viewport.



## -parameters




### -param contentSize [in]

The bounding rectangle of the content.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The default bounding rectangle is (-<a href="https://msdn.microsoft.com/library/ms858507(v=MSDN.10).aspx">FLT_MAX</a>, -<a href="https://msdn.microsoft.com/library/ms858507(v=MSDN.10).aspx">FLT_MAX</a>, <a href="https://msdn.microsoft.com/library/ms858507(v=MSDN.10).aspx">FLT_MAX</a>, <a href="https://msdn.microsoft.com/library/ms858507(v=MSDN.10).aspx">FLT_MAX</a>).




## -see-also




<a href="https://msdn.microsoft.com/4d69a503-f998-4197-824f-4df48825c941">IDirectManipulationContent</a>
 

 


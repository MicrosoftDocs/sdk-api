---
UID: NF:d2d1_3.ID2D1GdiMetafile1.GetSourceBounds
title: ID2D1GdiMetafile1::GetSourceBounds
author: windows-sdk-content
description: Gets the bounds of the metafile in source space in DIPs. This corresponds to the frame rect in an EMF/EMF+.
old-location: direct2d\id2d1gdimetafile1_getsourcebounds.htm
tech.root: Direct2D
ms.assetid: 7e7502ee-678e-ce26-cc0b-266faa1c320b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetSourceBounds, GetSourceBounds method [Direct2D], GetSourceBounds method [Direct2D],ID2D1GdiMetafile1 interface, ID2D1GdiMetafile1 interface [Direct2D],GetSourceBounds method, ID2D1GdiMetafile1.GetSourceBounds, ID2D1GdiMetafile1::GetSourceBounds, d2d1_3/ID2D1GdiMetafile1::GetSourceBounds, direct2d.id2d1gdimetafile1_getsourcebounds
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1GdiMetafile1.GetSourceBounds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1_3.h
: 
- ID2D1GdiMetafile1.GetSourceBounds
: 
---

# ID2D1GdiMetafile1::GetSourceBounds


## -description


Gets the bounds of the metafile in source space in DIPs. This corresponds      
    to the frame rect in an EMF/EMF+.


## -parameters




### -param bounds [out]

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The bounds, in DIPs, of the metafile.


## -returns



Type: <b>HRESULT</b>

S_OK if successful, otherwise a failure HRESULT.




## -see-also




<a href="https://msdn.microsoft.com/36A454EC-7DE0-4610-B49C-7FBBD21C425C">ID2D1GdiMetafile</a>



<a href="https://msdn.microsoft.com/7a05abd6-ea75-8496-85c3-efa1e307482d">ID2D1GdiMetafile1</a>



<a href="http://msdn.microsoft.com/en-us/library/cc230724.aspx">[MS-EMFPLUS]: Enhanced Metafile Format Plus Extensions</a>



<a href="http://msdn.microsoft.com/en-us/library/cc230514.aspx">[MS-EMF]: Enhanced Metafile Format</a>
 

 


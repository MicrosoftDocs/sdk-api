---
UID: NF:d2d1effectauthor.ID2D1DrawInfo.SetResourceTexture
title: ID2D1DrawInfo::SetResourceTexture
author: windows-sdk-content
description: Sets the resource texture corresponding to the given shader texture index.
old-location: direct2d\id2d1drawinfo_setresourcetexture.htm
tech.root: direct2d
ms.assetid: 6E53577B-AD97-4530-8260-4A99B90E0581
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: ID2D1DrawInfo interface [Direct2D],SetResourceTexture method, ID2D1DrawInfo.SetResourceTexture, ID2D1DrawInfo::SetResourceTexture, SetResourceTexture, SetResourceTexture method [Direct2D], SetResourceTexture method [Direct2D],ID2D1DrawInfo interface, d2d1effectauthor/ID2D1DrawInfo::SetResourceTexture, direct2d.id2d1drawinfo_setresourcetexture
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1DrawInfo.SetResourceTexture
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DrawInfo::SetResourceTexture


## -description


Sets the resource texture corresponding to the given shader texture index.


## -parameters




### -param textureIndex

Type: <b>UINT32</b>

The index of the texture to be bound to the pixel shader.


### -param resourceTexture [in]

Type: <b><a href="https://msdn.microsoft.com/516FFBB4-1908-4574-BD4A-884C142204CD">ID2D1ResourceTexture</a>*</b>

The created resource texture.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9C7B8CE0-0D2D-4383-9BE1-25F86BCEF253">ID2D1DrawInfo</a>
 

 


---
UID: NF:dxgi1_2.IDXGIOutputDuplication.GetDesc
title: IDXGIOutputDuplication::GetDesc
author: windows-sdk-content
description: Retrieves a description of a duplicated output. This description specifies the dimensions of the surface that contains the desktop image.
old-location: direct3ddxgi\idxgioutputduplication_getdesc.htm
old-project: direct3ddxgi
ms.assetid: 40D2CF38-1528-48A4-BC0C-5D8CC132D0CB
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetDesc, GetDesc method [DXGI], GetDesc method [DXGI],IDXGIOutputDuplication interface, IDXGIOutputDuplication interface [DXGI],GetDesc method, IDXGIOutputDuplication.GetDesc, IDXGIOutputDuplication::GetDesc, direct3ddxgi.idxgioutputduplication_getdesc, dxgi1_2/IDXGIOutputDuplication::GetDesc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DXGI_OFFER_RESOURCE_PRIORITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIOutputDuplication.GetDesc
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIOutputDuplication::GetDesc


## -description


Retrieves a description of a duplicated output. This description specifies the dimensions of the surface that contains the desktop image.


## -parameters




### -param pDesc [out]

A pointer to a <a href="https://msdn.microsoft.com/003014E3-4322-4253-8D69-AE315CDFDA75">DXGI_OUTDUPL_DESC</a> structure that describes the duplicated output. This parameter must not be <b>NULL</b>.


## -returns



Returns nothing.




## -remarks



After an application creates an <a href="https://msdn.microsoft.com/02C4EC3D-D97F-4CFC-ABF5-03B44CE6A658">IDXGIOutputDuplication</a> interface, it calls <b>GetDesc</b> to retrieve the dimensions of the surface that contains the desktop image. The format of the desktop image is always <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_B8G8R8A8_UNORM</a>.




## -see-also




<a href="https://msdn.microsoft.com/02C4EC3D-D97F-4CFC-ABF5-03B44CE6A658">IDXGIOutputDuplication</a>
 

 


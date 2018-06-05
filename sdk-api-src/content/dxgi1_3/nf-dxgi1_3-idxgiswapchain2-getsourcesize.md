---
UID: NF:dxgi1_3.IDXGISwapChain2.GetSourceSize
title: IDXGISwapChain2::GetSourceSize
author: windows-sdk-content
description: Gets the source region used for the swap chain.
old-location: direct3ddxgi\idxgioutpu2_getsourcesize.htm
old-project: direct3ddxgi
ms.assetid: C7E9BC13-74E5-4981-8F87-390F95B71AE0
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: GetSourceSize, GetSourceSize method [DXGI], GetSourceSize method [DXGI],IDXGISwapChain2 interface, IDXGISwapChain2 interface [DXGI],GetSourceSize method, IDXGISwapChain2.GetSourceSize, IDXGISwapChain2::GetSourceSize, direct3ddxgi.idxgioutpu2_getsourcesize, dxgi1_3/IDXGISwapChain2::GetSourceSize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
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
req.typenames: DXGI_OVERLAY_SUPPORT_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxgi.lib
-	dxgi.dll
api_name:
-	IDXGISwapChain2.GetSourceSize
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChain2::GetSourceSize


## -description


Gets the source region used for the swap chain.

Use <b>GetSourceSize</b> to get the portion of the swap chain from which the operating system presents. The source rectangle is always defined by the region [0, 0, Width, Height]. Use <a href="https://msdn.microsoft.com/BD424F5A-9735-4E90-9FAD-A0B827D7AD80">SetSourceSize</a> to set this portion of the swap chain. 


## -parameters




### -param pWidth [out]

 The current width of the source region of the swap chain. This value can range from 1 to the overall width of the swap chain.


### -param pHeight [out]

The current height of the source region of the swap chain. This value can range from 1 to the overall height of the swap chain.


## -returns



 This method can return error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/1E14EAF6-5EEA-4B4A-8F5F-0BC779093654">IDXGISwapChain2</a>



<a href="https://msdn.microsoft.com/BD424F5A-9735-4E90-9FAD-A0B827D7AD80">SetSourceSize</a>
 

 


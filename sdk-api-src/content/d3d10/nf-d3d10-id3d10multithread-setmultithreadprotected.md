---
UID: NF:d3d10.ID3D10Multithread.SetMultithreadProtected
title: ID3D10Multithread::SetMultithreadProtected method
author: windows-driver-content
description: Turn multithreading on or off.
old-location: direct3d10\id3d10multithread_setmultithreadprotected.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10multithread_setmultithreadprotected.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 22302703-e7e4-5872-896b-8c2360171b16, ID3D10Multithread, ID3D10Multithread interface [Direct3D 10], SetMultithreadProtected method, ID3D10Multithread::SetMultithreadProtected, SetMultithreadProtected method [Direct3D 10], SetMultithreadProtected method [Direct3D 10], ID3D10Multithread interface, SetMultithreadProtected,ID3D10Multithread.SetMultithreadProtected, d3d10/ID3D10Multithread::SetMultithreadProtected, direct3d10.id3d10multithread_setmultithreadprotected
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10.h
req.include-header: 
req.target-type: Windows
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
req.typenames: D3D10_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10Multithread.SetMultithreadProtected
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Multithread::SetMultithreadProtected method


## -description


Turn multithreading on or off.


## -parameters




### -param bMTProtect [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

True to turn multithreading on, false to turn it off.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

True if multithreading was turned on prior to calling this method, false otherwise.




## -see-also




<a href="https://msdn.microsoft.com/ff4890fe-25a3-4515-b20d-45f68637e7b3">ID3D10Multithread Interface</a>
 

 


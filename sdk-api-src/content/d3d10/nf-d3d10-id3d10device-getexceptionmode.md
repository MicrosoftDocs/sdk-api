---
UID: NF:d3d10.ID3D10Device.GetExceptionMode
title: ID3D10Device::GetExceptionMode
author: windows-driver-content
description: Get the exception-mode flags.
old-location: direct3d10\id3d10device_getexceptionmode.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_getexceptionmode.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 54b3d5fb-a9f3-6db2-1a8d-4bbc06e45e39, GetExceptionMode, GetExceptionMode method [Direct3D 10], GetExceptionMode method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GetExceptionMode method, ID3D10Device.GetExceptionMode, ID3D10Device::GetExceptionMode, d3d10/ID3D10Device::GetExceptionMode, direct3d10.id3d10device_getexceptionmode
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
-	ID3D10Device.GetExceptionMode
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::GetExceptionMode


## -description


Get the exception-mode flags.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value that contains one or more exception flags; each flag specifies a condition which will cause an exception to be raised. The flags are listed in <a href="https://msdn.microsoft.com/80918203-e310-44f4-bcf4-88f2a7067379">D3D10_RAISE_FLAG</a>. A default value of 0 means there are no flags.




## -remarks



An exception-mode flag is used to elevate an error condition to a non-continuable exception. 




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 


---
UID: NF:d3d11.ID3D11Device.GetExceptionMode
title: ID3D11Device::GetExceptionMode
author: windows-sdk-content
description: Get the exception-mode flags.
old-location: direct3d11\id3d11device_getexceptionmode.htm
old-project: direct3d11
ms.assetid: c5deddde-4355-4a34-b40a-50006029d590
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 00dedc29-911b-cd5e-0b45-8f2505b70599, GetExceptionMode, GetExceptionMode method [Direct3D 11], GetExceptionMode method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],GetExceptionMode method, ID3D11Device.GetExceptionMode, ID3D11Device::GetExceptionMode, d3d11/ID3D11Device::GetExceptionMode, direct3d11.id3d11device_getexceptionmode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11.h
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.GetExceptionMode
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device::GetExceptionMode


## -description


Get the exception-mode flags.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value that contains one or more exception flags; each flag specifies a condition which will cause an exception to be raised. The flags are listed in <a href="https://msdn.microsoft.com/cdb88a12-153d-4f92-89c8-d3dab1b6bed5">D3D11_RAISE_FLAG</a>. A default value of 0 means there are no flags.




## -remarks



An exception-mode flag is used to elevate an error condition to a non-continuable exception. 




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 


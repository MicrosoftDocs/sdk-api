---
UID: NE:d3d10.D3D10_ASYNC_GETDATA_FLAG
title: D3D10_ASYNC_GETDATA_FLAG
author: windows-sdk-content
description: Optional flags that control the behavior of ID3D10Asynchronous::GetData.
old-location: direct3d10\d3d10_async_getdata_flag.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_async_getdata_flag.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D10_ASYNC_GETDATA_DONOTFLUSH, D3D10_ASYNC_GETDATA_FLAG, D3D10_ASYNC_GETDATA_FLAG enumeration [Direct3D 10], d0797ad1-e1be-88a9-fb81-7dba0cb6c9ea, d3d10/D3D10_ASYNC_GETDATA_DONOTFLUSH, d3d10/D3D10_ASYNC_GETDATA_FLAG, direct3d10.d3d10_async_getdata_flag
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_ASYNC_GETDATA_FLAG
product: Windows
targetos: Windows
req.typenames: D3D10_ASYNC_GETDATA_FLAG
req.redist: 
---

# D3D10_ASYNC_GETDATA_FLAG enumeration


## -description


Optional flags that control the behavior of <a href="https://msdn.microsoft.com/f8993ac8-3632-48d0-a583-08f117e8f587">ID3D10Asynchronous::GetData</a>.


## -enum-fields




### -field D3D10_ASYNC_GETDATA_DONOTFLUSH

Do not flush the command buffer. This can potentially cause an infinite loop if GetData is continually called until it returns S_OK as there may still be commands in the command buffer that need to be processed in order for GetData to return S_OK. Since the commands in the command buffer are not flushed they will not be processed and therefore GetData will never return S_OK.


## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>
 

 


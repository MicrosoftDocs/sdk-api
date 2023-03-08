---
UID: NF:d3d10.ID3D10Device.GetExceptionMode
title: ID3D10Device::GetExceptionMode (d3d10.h)
description: Get the exception-mode flags. (ID3D10Device.GetExceptionMode)
helpviewer_keywords: ["54b3d5fb-a9f3-6db2-1a8d-4bbc06e45e39","GetExceptionMode","GetExceptionMode method [Direct3D 10]","GetExceptionMode method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","GetExceptionMode method","ID3D10Device.GetExceptionMode","ID3D10Device::GetExceptionMode","d3d10/ID3D10Device::GetExceptionMode","direct3d10.id3d10device_getexceptionmode"]
old-location: direct3d10\id3d10device_getexceptionmode.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_getexceptionmode.htm
ms.date: 12/05/2018
ms.keywords: 54b3d5fb-a9f3-6db2-1a8d-4bbc06e45e39, GetExceptionMode, GetExceptionMode method [Direct3D 10], GetExceptionMode method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GetExceptionMode method, ID3D10Device.GetExceptionMode, ID3D10Device::GetExceptionMode, d3d10/ID3D10Device::GetExceptionMode, direct3d10.id3d10device_getexceptionmode
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::GetExceptionMode
 - d3d10/ID3D10Device::GetExceptionMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.GetExceptionMode
---

# ID3D10Device::GetExceptionMode


## -description

Get the exception-mode flags.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value that contains one or more exception flags; each flag specifies a condition which will cause an exception to be raised. The flags are listed in <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_raise_flag">D3D10_RAISE_FLAG</a>. A default value of 0 means there are no flags.

## -remarks

An exception-mode flag is used to elevate an error condition to a non-continuable exception.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>

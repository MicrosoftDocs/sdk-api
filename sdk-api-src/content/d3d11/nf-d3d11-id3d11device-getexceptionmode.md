---
UID: NF:d3d11.ID3D11Device.GetExceptionMode
title: ID3D11Device::GetExceptionMode (d3d11.h)
description: Get the exception-mode flags. (ID3D11Device.GetExceptionMode)
helpviewer_keywords: ["00dedc29-911b-cd5e-0b45-8f2505b70599","GetExceptionMode","GetExceptionMode method [Direct3D 11]","GetExceptionMode method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","GetExceptionMode method","ID3D11Device.GetExceptionMode","ID3D11Device::GetExceptionMode","d3d11/ID3D11Device::GetExceptionMode","direct3d11.id3d11device_getexceptionmode"]
old-location: direct3d11\id3d11device_getexceptionmode.htm
tech.root: direct3d11
ms.assetid: c5deddde-4355-4a34-b40a-50006029d590
ms.date: 12/05/2018
ms.keywords: 00dedc29-911b-cd5e-0b45-8f2505b70599, GetExceptionMode, GetExceptionMode method [Direct3D 11], GetExceptionMode method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],GetExceptionMode method, ID3D11Device.GetExceptionMode, ID3D11Device::GetExceptionMode, d3d11/ID3D11Device::GetExceptionMode, direct3d11.id3d11device_getexceptionmode
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device::GetExceptionMode
 - d3d11/ID3D11Device::GetExceptionMode
dev_langs:
 - c++
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
---

# ID3D11Device::GetExceptionMode


## -description

Get the exception-mode flags.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value that contains one or more exception flags; each flag specifies a condition which will cause an exception to be raised. The flags are listed in <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_raise_flag">D3D11_RAISE_FLAG</a>. A default value of 0 means there are no flags.

## -remarks

An exception-mode flag is used to elevate an error condition to a non-continuable exception.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>

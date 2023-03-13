---
UID: NF:d3d11.ID3D11Device.SetExceptionMode
title: ID3D11Device::SetExceptionMode (d3d11.h)
description: Get the exception-mode flags. (ID3D11Device.SetExceptionMode)
helpviewer_keywords: ["ID3D11Device interface [Direct3D 11]","SetExceptionMode method","ID3D11Device.SetExceptionMode","ID3D11Device::SetExceptionMode","SetExceptionMode","SetExceptionMode method [Direct3D 11]","SetExceptionMode method [Direct3D 11]","ID3D11Device interface","a5c01332-6f00-24e5-1424-e59e0f7353bd","d3d11/ID3D11Device::SetExceptionMode","direct3d11.id3d11device_setexceptionmode"]
old-location: direct3d11\id3d11device_setexceptionmode.htm
tech.root: direct3d11
ms.assetid: a442a5dc-7931-4464-a6e7-76441e61da5b
ms.date: 12/05/2018
ms.keywords: ID3D11Device interface [Direct3D 11],SetExceptionMode method, ID3D11Device.SetExceptionMode, ID3D11Device::SetExceptionMode, SetExceptionMode, SetExceptionMode method [Direct3D 11], SetExceptionMode method [Direct3D 11],ID3D11Device interface, a5c01332-6f00-24e5-1424-e59e0f7353bd, d3d11/ID3D11Device::SetExceptionMode, direct3d11.id3d11device_setexceptionmode
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
 - ID3D11Device::SetExceptionMode
 - d3d11/ID3D11Device::SetExceptionMode
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
 - ID3D11Device.SetExceptionMode
---

# ID3D11Device::SetExceptionMode


## -description

Get the exception-mode flags.

## -parameters

### -param RaiseFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value that contains one or more exception flags; each flag specifies a condition which will cause an exception to be raised. The flags are listed in <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_raise_flag">D3D11_RAISE_FLAG</a>. A default value of 0 means there are no flags.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

Set an exception-mode flag to elevate an error condition to a non-continuable exception. 

Whenever an error occurs, a Direct3D device enters the DEVICEREMOVED state and if the appropriate exception flag has been set, an exception is raised. A raised exception is designed to terminate an application. Before termination, the last chance an application has to persist data is by using an UnhandledExceptionFilter (see <a href="/windows/desktop/Debug/structured-exception-handling">Structured Exception Handling</a>). In general, UnhandledExceptionFilters are leveraged to try to persist data when an application is crashing (to disk, for example). Any code that executes during an UnhandledExceptionFilter is not guaranteed to reliably execute (due to possible process corruption). Any data that the UnhandledExceptionFilter manages to persist, before the UnhandledExceptionFilter crashes again, should be treated as suspect, and therefore inspected by a new, non-corrupted process to see if it is usable.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>

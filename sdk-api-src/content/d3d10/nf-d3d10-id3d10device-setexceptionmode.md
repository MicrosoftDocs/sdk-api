---
UID: NF:d3d10.ID3D10Device.SetExceptionMode
title: ID3D10Device::SetExceptionMode (d3d10.h)
description: Get the exception-mode flags.
helpviewer_keywords: ["450093c6-975d-3a2a-6e09-2d2267d36bae","ID3D10Device interface [Direct3D 10]","SetExceptionMode method","ID3D10Device.SetExceptionMode","ID3D10Device::SetExceptionMode","SetExceptionMode","SetExceptionMode method [Direct3D 10]","SetExceptionMode method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::SetExceptionMode","direct3d10.id3d10device_setexceptionmode"]
old-location: direct3d10\id3d10device_setexceptionmode.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_setexceptionmode.htm
ms.date: 12/05/2018
ms.keywords: 450093c6-975d-3a2a-6e09-2d2267d36bae, ID3D10Device interface [Direct3D 10],SetExceptionMode method, ID3D10Device.SetExceptionMode, ID3D10Device::SetExceptionMode, SetExceptionMode, SetExceptionMode method [Direct3D 10], SetExceptionMode method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::SetExceptionMode, direct3d10.id3d10device_setexceptionmode
f1_keywords:
- d3d10/ID3D10Device.SetExceptionMode
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D10.lib
- D3D10.dll
api_name:
- ID3D10Device.SetExceptionMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Device::SetExceptionMode


## -description


Get the exception-mode flags.


## -parameters




### -param RaiseFlags [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A value that contains one or more exception flags; each flag specifies a condition which will cause an exception to be raised. The flags are listed in <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_raise_flag">D3D10_RAISE_FLAG</a>. A default value of 0 means there are no flags.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -remarks



Set an exception-mode flag to elevate an error condition to a non-continuable exception. 

Whenever an error occurs, a Direct3D device enters the DEVICEREMOVED state and if the appropriate exception flag has been set, an exception is raised. A raised exception is designed to terminate an application. Before termination, the last chance an application has to persist data is by using an UnhandledExceptionFilter (see <a href="https://docs.microsoft.com/windows/desktop/Debug/structured-exception-handling">Structured Exception Handling</a>). In general, UnhandledExceptionFilters are leveraged to try to persist data when an application is crashing (to disk, for example). Any code that executes during an UnhandledExceptionFilter is not guaranteed to reliably execute (due to possible process corruption). Any data that the UnhandledExceptionFilter manages to persist, before the UnhandledExceptionFilter crashes again, should be treated as suspect, and therefore inspected by a new, non-corrupted process to see if it is usable.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
 

 


---
UID: NF:d3d11.ID3D11Device.SetExceptionMode
title: ID3D11Device::SetExceptionMode
author: windows-sdk-content
description: Get the exception-mode flags.
old-location: direct3d11\id3d11device_setexceptionmode.htm
old-project: direct3d11
ms.assetid: a442a5dc-7931-4464-a6e7-76441e61da5b
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: ID3D11Device interface [Direct3D 11],SetExceptionMode method, ID3D11Device.SetExceptionMode, ID3D11Device::SetExceptionMode, SetExceptionMode, SetExceptionMode method [Direct3D 11], SetExceptionMode method [Direct3D 11],ID3D11Device interface, a5c01332-6f00-24e5-1424-e59e0f7353bd, d3d11/ID3D11Device::SetExceptionMode, direct3d11.id3d11device_setexceptionmode
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11Device.SetExceptionMode
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device::SetExceptionMode


## -description


Get the exception-mode flags.


## -parameters




### -param RaiseFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value that contains one or more exception flags; each flag specifies a condition which will cause an exception to be raised. The flags are listed in <a href="https://msdn.microsoft.com/cdb88a12-153d-4f92-89c8-d3dab1b6bed5">D3D11_RAISE_FLAG</a>. A default value of 0 means there are no flags.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



Set an exception-mode flag to elevate an error condition to a non-continuable exception. 

Whenever an error occurs, a Direct3D device enters the DEVICEREMOVED state and if the appropriate exception flag has been set, an exception is raised. A raised exception is designed to terminate an application. Before termination, the last chance an application has to persist data is by using an UnhandledExceptionFilter (see <a href="http://msdn2.microsoft.com/en-us/library/ms680657.aspx">Structured Exception Handling</a>). In general, UnhandledExceptionFilters are leveraged to try to persist data when an application is crashing (to disk, for example). Any code that executes during an UnhandledExceptionFilter is not guaranteed to reliably execute (due to possible process corruption). Any data that the UnhandledExceptionFilter manages to persist, before the UnhandledExceptionFilter crashes again, should be treated as suspect, and therefore inspected by a new, non-corrupted process to see if it is usable.




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 


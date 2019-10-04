---
UID: NF:cfapi.CfGetWin32HandleFromProtectedHandle
title: CfGetWin32HandleFromProtectedHandle function (cfapi.h)
author: windows-sdk-content
description: Converts a protected handle to a Win32 handle so that it can be used with all handle-based Win32 APIs.
old-location: cloudapi\cfgetwin32handlefromprotectedhandle.htm
tech.root: cfApi
ms.assetid: 8C54B6F3-7709-4021-8965-E96B74DD3319
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CfGetWin32HandleFromProtectedHandle, CfGetWin32HandleFromProtectedHandle function, cfapi/CfGetWin32HandleFromProtectedHandle, cloudApi.cfgetwin32handlefromprotectedhandle
ms.topic: function
f1_keywords: 
 - "cfapi/CfGetWin32HandleFromProtectedHandle"
dev_langs:
 - c++
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfGetWin32HandleFromProtectedHandle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CfGetWin32HandleFromProtectedHandle function


## -description


Converts a protected handle to a Win32 handle so that it can be used with all handle-based Win32 APIs. 


## -parameters




### -param ProtectedHandle [in]

The protected handle to be converted.


## -returns



The corresponding Win32 handle.




## -remarks



The caller must have referenced the protected handle prior to this call using <a href="https://docs.microsoft.com/windows/desktop/api/cfapi/nf-cfapi-cfreferenceprotectedhandle">CfReferenceProtectedHandle</a> to ensure that the use of the Win32 handle is tracked, and the Win32 API call that consumes the Win32 handle is synchronized with the oplock break notification acknowledgment. 

The caller must release the reference on the protected handle after being done with the Win32 handle using <a href="https://docs.microsoft.com/windows/desktop/api/cfapi/nf-cfapi-cfreleaseprotectedhandle">CfReleaseProtectedHandle</a>. 

In no circumstances should the caller close the Win32 handle returned using <a href="https://docs.microsoft.com/windows/desktop/api/cfapi/nf-cfapi-cfclosehandle">CfCloseHandle</a>.




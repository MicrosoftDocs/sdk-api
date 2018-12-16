---
UID: NF:cfapi.CfGetWin32HandleFromProtectedHandle
title: CfGetWin32HandleFromProtectedHandle function
author: windows-sdk-content
description: Converts a protected handle to a Win32 handle so that it can be used with all handle-based Win32 APIs.
old-location: cloudapi\cfgetwin32handlefromprotectedhandle.htm
tech.root: cfApi
ms.assetid: 8C54B6F3-7709-4021-8965-E96B74DD3319
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CfGetWin32HandleFromProtectedHandle, CfGetWin32HandleFromProtectedHandle function, cfapi/CfGetWin32HandleFromProtectedHandle, cloudApi.cfgetwin32handlefromprotectedhandle
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



The caller must have referenced the protected handle prior to this call using <a href="https://msdn.microsoft.com/C6281FD6-3A37-4D90-9B19-03DD23949C39">CfReferenceProtectedHandle</a> to ensure that the use of the Win32 handle is tracked, and the Win32 API call that consumes the Win32 handle is synchronized with the oplock break notification acknowledgment. 

The caller must release the reference on the protected handle after being done with the Win32 handle using <a href="https://msdn.microsoft.com/BB63C5EE-92D7-4051-8198-09F50BBC75C5">CfReleaseProtectedHandle</a>. 

In no circumstances should the caller close the Win32 handle returned using <a href="https://msdn.microsoft.com/ECBEF685-0769-4AEA-8A0F-D5FBB70CBB09">CfCloseHandle</a>.




---
UID: NF:cfapi.CfCloseHandle
title: CfCloseHandle function (cfapi.h)
author: windows-sdk-content
description: Closes the file or directory handle returned by CfOpenFileWithOplock. This should not be used with standard Win32 file handles, only on handles used within CfApi.h.
old-location: cloudapi\cfclosehandle.htm
tech.root: cfApi
ms.assetid: ECBEF685-0769-4AEA-8A0F-D5FBB70CBB09
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CfCloseHandle, CfCloseHandle function, cfapi/CfCloseHandle, cloudApi.cfclosehandle
ms.topic: function
f1_keywords: 
 - "cfapi/CfCloseHandle"
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
 - CfCloseHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CfCloseHandle function


## -description


Closes the file or directory handle returned by <a href="https://docs.microsoft.com/windows/desktop/api/cfapi/nf-cfapi-cfopenfilewithoplock">CfOpenFileWithOplock</a>. This should not be used with standard Win32 file handles, only on handles used within CfApi.h.


## -parameters




### -param FileHandle [in]

The file or directory handle to be closed.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




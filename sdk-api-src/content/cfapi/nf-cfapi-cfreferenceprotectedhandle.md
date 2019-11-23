---
UID: NF:cfapi.CfReferenceProtectedHandle
title: CfReferenceProtectedHandle function (cfapi.h)

description: Allows the caller to reference a protected handle to a Win32 handle which can be used with non-CfApi Win32 APIs.
old-location: cloudapi\cfreferenceprotectedhandle.htm
tech.root: cfApi
ms.assetid: C6281FD6-3A37-4D90-9B19-03DD23949C39

ms.date: 12/05/2018
ms.keywords: CfReferenceProtectedHandle, CfReferenceProtectedHandle function, cfapi/CfReferenceProtectedHandle, cloudApi.cfreferenceprotectedhandle
ms.topic: function
f1_keywords: 
 - "cfapi/CfReferenceProtectedHandle"
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
 - CfReferenceProtectedHandle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CfReferenceProtectedHandle function


## -description


Allows the caller to reference a protected handle to a Win32 handle which can be used with non-CfApi Win32 APIs. 


## -parameters




### -param ProtectedHandle [in]

The protected handle of a placeholder file.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Every <b>CfReferenceProtectedHandle</b> call must be matched  with a <a href="https://docs.microsoft.com/windows/desktop/api/cfapi/nf-cfapi-cfreleaseprotectedhandle">CfReleaseProtectedHandle</a> call. It is not recommended to reference a protected handle for a long period of time, as doing so will prevent the oplock break notification from being acknowledged.

 The caller should instead break up long running tasks into smaller sub-tasks and reference/release the protected handle for each sub-task.




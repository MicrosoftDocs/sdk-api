---
UID: NF:cfapi.CfRevertPlaceholder
title: CfRevertPlaceholder function (cfapi.h)
author: windows-sdk-content
description: Reverts a placeholder back to a regular file, stripping away all special characteristics such as the reparse tag, the file identity, etc.
old-location: cloudapi\cfrevertplaceholder.htm
tech.root: cfApi
ms.assetid: D5404BB6-A066-4B5F-A355-A11A107610CE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CfRevertPlaceholder, CfRevertPlaceholder function, cfapi/CfRevertPlaceholder, cloudApi.cfrevertplaceholder
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
 - CfRevertPlaceholder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CfRevertPlaceholder function


## -description


Reverts a placeholder back to a regular file, stripping away all special characteristics such as the reparse tag, the file identity, etc.


## -parameters




### -param FileHandle [in]

A handle to the file or directory placeholder that is about to be reverted to normal file or directory. An attribute or no-access handle is sufficient.


### -param RevertFlags [in]

Placeholder revert flags.


### -param Overlapped [in, out, optional]

When specified and combined with an asynchronous <i>FileHandle</i>, <i>Overlapped</i> allows the platform to perform the <b>CfRevertPlaceholder</b> call asynchronously. See the Remarks for more details.

If not specified, the platform will perform the API call synchronously, regardless of how the handle was created.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The caller must have WRITE_DATA or WRITE_DAC access to the placeholder to be reverted.

If the placeholder is not already fully hydrated at the time of the call, then the filter will send a FETCH_DATA callback to the sync provider  to hydrate the file.  If the file can’t be hydrated, the revert will fail.

If the API returns HRESULT_FROM_WIN32(ERROR_IO_PENDING) when using <i>Overlapped</i> asynchronously, the caller can then wait using <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>. 






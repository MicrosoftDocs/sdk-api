---
UID: NF:cfapi.CfGetTransferKey
title: CfGetTransferKey function (cfapi.h)
author: windows-sdk-content
description: Initiates a transfer of data into a placeholder file or folder.
old-location: cloudapi\cfgettransferkey.htm
tech.root: cfApi
ms.assetid: 07DDC46A-0C10-4677-A4B0-5A0406BBDAB7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CfGetTransferKey, CfGetTransferKey function, cfapi/CfGetTransferKey, cloudApi.cfgettransferkey
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
 - CfGetTransferKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CfGetTransferKey function


## -description


Initiates a transfer of data into a placeholder file or folder.


## -parameters




### -param FileHandle [in]

The file handle of the placeholder.


### -param TransferKey [out]

An opaque handle to the placeholder to be serviced.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>CfGetTransferKey</b> is used as an alternative to <a href="https://msdn.microsoft.com/4FFD7580-BF59-48D0-B6D7-516559914096">CfHydratePlaceholder</a> to proactively initiate data transfer into a placeholder.

A sync provider should have READ_DATA or WRITE_DAC access to the file whose transfer key is to be obtained or <b>CfGetTransferKey</b> will be failed with HRESULT(ERROR_CLOUD_FILE_ACCESS_DENIED).

The <i>TransferKey</i> is valid as long as the <i>FileHandle</i> used to obtain it remains open. The sync provider must pass the <i>TransferKey</i> to <a href="https://msdn.microsoft.com/6AC8958D-B060-4468-9811-9BAB0E6A06D3">CfExecute</a> to perform the desired operation on the placholder file or folder.  When a <i>TransferKey</i> is no longer being used, it must be released using <a href="https://msdn.microsoft.com/53B40C34-EB1F-445B-B1B3-B539C2FADECE">CfReleaseTransferKey</a>.




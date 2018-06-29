---
UID: NF:cfapi.CfReleaseTransferKey
title: CfReleaseTransferKey function
author: windows-sdk-content
description: Releases a transfer key obtained by CfGetTransferKey.
old-location: cloudapi\cfreleasetransferkey.htm
old-project: cfApi
ms.assetid: 53B40C34-EB1F-445B-B1B3-B539C2FADECE
ms.author: windowssdkdev
ms.date: 02/26/2018
ms.keywords: CfReleaseTransferKey, CfReleaseTransferKey function, cfapi/CfReleaseTransferKey, cloudApi.cfreleasetransferkey
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CF_UPDATE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfReleaseTransferKey
product: Windows
targetos: Windows
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
---

# CfReleaseTransferKey function


## -description


Releases a transfer key obtained by <a href="https://msdn.microsoft.com/07DDC46A-0C10-4677-A4B0-5A0406BBDAB7">CfGetTransferKey</a>.


## -parameters




### -param FileHandle [in]

The file handle of the placeholder.


### -param TransferKey [in]

An opaque handle to the placeholder.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




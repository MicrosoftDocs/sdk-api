---
UID: NF:cfapi.CfGetPlaceholderInfo
title: CfGetPlaceholderInfo function (cfapi.h)
description: Gets various characteristics of a placeholder file or folder.
helpviewer_keywords: ["CfGetPlaceholderInfo","CfGetPlaceholderInfo function","cfapi/CfGetPlaceholderInfo","cloudApi.cfgetplaceholderinfo"]
old-location: cloudapi\cfgetplaceholderinfo.htm
tech.root: cloudapi
ms.assetid: D82269CF-8056-46CF-9832-AAE8767A854B
ms.date: 12/05/2018
ms.keywords: CfGetPlaceholderInfo, CfGetPlaceholderInfo function, cfapi/CfGetPlaceholderInfo, cloudApi.cfgetplaceholderinfo
f1_keywords:
- cfapi/CfGetPlaceholderInfo
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
- CfGetPlaceholderInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CfGetPlaceholderInfo function


## -description


Gets various characteristics of a placeholder file or folder.


## -parameters




### -param FileHandle [in]

A handle to the placeholder whose information will be queried.


### -param InfoClass [in]

Placeholder information. This can be set to either <a href="https://docs.microsoft.com/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_standard_info">CF_PLACEHOLDER_STANDARD_INFO</a> or <a href="https://docs.microsoft.com/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_basic_info">CF_PLACEHOLDER_BASIC_INFO</a>.


### -param InfoBuffer [out]

A pointer to a buffer that will receive information.


### -param InfoBufferLength [in]

The length of the <i>InfoBuffer</i>, in bytes.


### -param ReturnedLength [out, optional]

The number of bytes returned in the <i>InfoBuffer</i>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




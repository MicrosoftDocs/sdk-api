---
UID: NF:cfapi.CfGetPlaceholderInfo
title: CfGetPlaceholderInfo function
author: windows-sdk-content
description: Gets various characteristics of a placeholder file or folder.
old-location: cloudapi\cfgetplaceholderinfo.htm
tech.root: cfApi
ms.assetid: D82269CF-8056-46CF-9832-AAE8767A854B
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CfGetPlaceholderInfo, CfGetPlaceholderInfo function, cfapi/CfGetPlaceholderInfo, cloudApi.cfgetplaceholderinfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CfGetPlaceholderInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CfGetPlaceholderInfo function


## -description


Gets various characteristics of a placeholder file or folder.


## -parameters




### -param FileHandle [in]

A handle to the placeholder whose information will be queried.


### -param InfoClass [in]

Placeholder information. This can be set to either <a href="https://msdn.microsoft.com/F0CDC9CD-7D31-4854-9568-8F13516C6D15">CF_PLACEHOLDER_STANDARD_INFO</a> or <a href="https://msdn.microsoft.com/77367235-342D-4BBC-B910-FE798E14B588">CF_PLACEHOLDER_BASIC_INFO</a>.


### -param InfoBuffer [out]

A pointer to a buffer that will receive information.


### -param InfoBufferLength [in]

The length of the <i>InfoBuffer</i>, in bytes.


### -param ReturnedLength [out, optional]

The number of bytes returned in the <i>InfoBuffer</i>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




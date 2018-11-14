---
UID: NS:cfapi.CF_PLACEHOLDER_BASIC_INFO
title: CF_PLACEHOLDER_BASIC_INFO
author: windows-sdk-content
description: Basic placeholder information.
old-location: cloudapi\cf_placeholder_basic_info.htm
tech.root: cfApi
ms.assetid: 77367235-342D-4BBC-B910-FE798E14B588
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: CF_PLACEHOLDER_BASIC_INFO, CF_PLACEHOLDER_BASIC_INFO structure, cfapi/CF_PLACEHOLDER_BASIC_INFO, cloudApi.cf_placeholder_basic_info
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_PLACEHOLDER_BASIC_INFO
product: Windows
targetos: Windows
req.typenames: CF_PLACEHOLDER_BASIC_INFO
req.redist: 
---

# CF_PLACEHOLDER_BASIC_INFO structure


## -description


Basic placeholder information.


## -struct-fields




### -field PinState

The pin state of the placeholder. See <a href="https://msdn.microsoft.com/8B279914-E23A-479B-8621-E83DE1978597">CfSetPinState</a> for more details.


### -field InSyncState

The in-sync state of the placeholder. see <a href="https://msdn.microsoft.com/1CB7955D-E530-4F34-8D67-BC608F8B6AF1">CfSetInSyncState</a> for more details.


### -field FileId

A 64-bit volume wide non-volatile number that uniquely identifies a file or directory.


### -field SyncRootFileId

The file ID of the sync root directory that contains the file whose placeholder information is to be queried.


### -field FileIdentityLength

Length, in bytes, of the FileIdentity.


### -field FileIdentity

 




#### - FileIdentity[1]

An opaque blob supplied by the sync provider to the platform when the placeholder was created. File identity is provided for all sync provider callbacks.


---
UID: NE:cfapi.CF_CONVERT_FLAGS
title: CF_CONVERT_FLAGS
author: windows-sdk-content
description: Normal file/directory to placeholder file/directory conversion flags.
old-location: cloudapi\cf_convert_flags.htm
old-project: cfApi
ms.assetid: 0342BF0B-509A-4F8D-9557-54E534A3DDFE
ms.author: windowssdkdev
ms.date: 02/26/2018
ms.keywords: CF_CONVERT_FLAGS, CF_CONVERT_FLAGS enumeration, CF_CONVERT_FLAG_DEHYDRATE, CF_CONVERT_FLAG_ENABLE_ON_DEMAND_POPULATION, CF_CONVERT_FLAG_MARK_IN_SYNC, CF_CONVERT_FLAG_NONE, cfapi/CF_CONVERT_FLAGS, cfapi/CF_CONVERT_FLAG_DEHYDRATE, cfapi/CF_CONVERT_FLAG_ENABLE_ON_DEMAND_POPULATION, cfapi/CF_CONVERT_FLAG_MARK_IN_SYNC, cfapi/CF_CONVERT_FLAG_NONE, cloudApi.cf_convert_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: CF_CONVERT_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_CONVERT_FLAGS
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
---

# CF_CONVERT_FLAGS enumeration


## -description


Normal file/directory to placeholder file/directory conversion flags.


## -enum-fields




### -field CF_CONVERT_FLAG_NONE

No conversion flags.


### -field CF_CONVERT_FLAG_MARK_IN_SYNC

The platform marks the converted placeholder as in sync with cloud upon a successful conversion of the file.


### -field CF_CONVERT_FLAG_DEHYDRATE

Applicable to files only. When specified, the platform dehydrates the file after converting it to a placeholder successfully. The caller must acquire an exclusive handle when specifying this flag or data corruptions can occur. Note that the platform does not validate the exclusiveness of the handle.


### -field CF_CONVERT_FLAG_ENABLE_ON_DEMAND_POPULATION

Applicable for directories only. When specified, it marks the converted placeholder directory as partially populated such that any future access to it will result in a FETCH_PLACEHOLDERS callback sent to the sync provider.


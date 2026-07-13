---
UID: NS:cfapi.CF_FILE_RANGE
title: CF_FILE_RANGE (cfapi.h)
description: Specifies a range of data in a placeholder file.
helpviewer_keywords: ["CF_FILE_RANGE","CF_FILE_RANGE structure","cfapi/CF_FILE_RANGE","cloudApi.cf_file_range"]
old-location: cloudapi\cf_file_range.htm
tech.root: cloudapi
ms.assetid: DAE43446-725E-490B-AE1B-EA6CB31F4358
ms.date: 12/05/2018
ms.keywords: CF_FILE_RANGE, CF_FILE_RANGE structure, cfapi/CF_FILE_RANGE, cloudApi.cf_file_range
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
targetos: Windows
req.typenames: CF_FILE_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_FILE_RANGE
 - cfapi/CF_FILE_RANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_FILE_RANGE
---

# CF_FILE_RANGE structure

## -description

Specifies a range of data in a placeholder file.

## -struct-fields

### -field StartingOffset

The offset of the starting point of the data.

### -field Length

The length of the data, in bytes.

## -see-also

[CfUpdatePlaceholder](nf-cfapi-cfupdateplaceholder.md)

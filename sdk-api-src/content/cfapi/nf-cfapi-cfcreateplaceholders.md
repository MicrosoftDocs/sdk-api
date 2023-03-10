---
UID: NF:cfapi.CfCreatePlaceholders
title: CfCreatePlaceholders function (cfapi.h)
description: Creates one or more new placeholder files or directories under a sync root tree.
helpviewer_keywords: ["CfCreatePlaceholders","CfCreatePlaceholders function","cfapi/CfCreatePlaceholders","cloudApi.cfcreateplaceholders"]
old-location: cloudapi\cfcreateplaceholders.htm
tech.root: cloudapi
ms.assetid: 96A6F62E-7F14-40B5-AB57-260DC9B1DF89
ms.date: 12/05/2018
ms.keywords: CfCreatePlaceholders, CfCreatePlaceholders function, cfapi/CfCreatePlaceholders, cloudApi.cfcreateplaceholders
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CfCreatePlaceholders
 - cfapi/CfCreatePlaceholders
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfCreatePlaceholders
---

# CfCreatePlaceholders function


## -description

Creates one or more new placeholder files or directories under a sync root tree.

## -parameters

### -param BaseDirectoryPath [in]

Path to the local directory in which the placeholders are created. This path must be under the sync root of the provider.

### -param PlaceholderArray [in, out]

On successful creation, the <i>PlaceholderArray</i> contains the final USN value and a STATUS_OK message. On return, this array contains an HRESULT value describing whether the placeholder was created or not.

### -param PlaceholderCount [in]

The count of placeholders in the <i>PlaceholderArray</i>.

### -param CreateFlags [in]

Flags for configuring the  creation of a placeholder.

### -param EntriesProcessed [out]

The number of entries processed, including failed entries.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Creating a placeholder with this function is preferred compared to creating a new file with <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> and then converting it to a placeholder with <a href="/windows/desktop/api/cfapi/nf-cfapi-cfconverttoplaceholder">CfConvertToPlaceholder</a>; both for efficiency and because it eliminates the time window where the file is not a placeholder.  The function can also create multiple files or directories in a batch, which can also be more efficient.

This function is useful when performing an initial sync of files or directories from the cloud down to the client, or when syncing down a newly created single file or directory from the cloud.

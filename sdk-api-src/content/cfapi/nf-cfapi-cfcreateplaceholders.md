---
UID: NF:cfapi.CfCreatePlaceholders
title: CfCreatePlaceholders function
author: windows-driver-content
description: Creates one or more new placeholder files or directories under a sync root tree.
old-location: cloudapi\cfcreateplaceholders.htm
old-project: cfApi
ms.assetid: 96A6F62E-7F14-40B5-AB57-260DC9B1DF89
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CfCreatePlaceholders, CfCreatePlaceholders function, cfapi/CfCreatePlaceholders, cloudApi.cfcreateplaceholders
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
req.typenames: CF_PLACEHOLDER_RANGE_INFO_CLASS, *PCF_PLACEHOLDER_RANGE_INFO_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	CldApi.dll
api_name:
-	CfCreatePlaceholders
product: Windows
targetos: Windows
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
---

# CfCreatePlaceholders function


## -description


Creates one or more new placeholder files or directories under a sync root tree.


## -parameters




### -param BaseDirectoryPath [in]

Local directory path under which placeholders are created.


### -param PlaceholderArray [in, out]

On successful creation, the <i>PlaceholderArray</i> contains the final USN value and a STATUS_OK message. On return, this array contains an HRESULT value describing whether the placeholder was created or not.


### -param PlaceholderCount [in]

The count of placeholders in the <i>PlaceholderArray</i>.


### -param CreateFlags [in]

Flags for configuring the  creation of a placeholder.


### -param EntriesProcessed [out]

The number of entries processed, including failed entries.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creating a placeholder with this function is preferred compared to creating a new file with <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> and then converting it to a placeholder with <a href="https://msdn.microsoft.com/FDDE9CB0-E1A2-46D6-94E0-228495675271">CfConvertToPlaceholder</a>; both for efficiency and because it eliminates the time window where the file is not a placeholder.  The function can also create multiple files or directories in a batch, which can also be more efficient.

This function is useful when performing an initial sync of files or directories from the cloud down to the client, or when syncing down a newly created single file or directory from the cloud.




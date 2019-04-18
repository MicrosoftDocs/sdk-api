---
UID: NF:srrestoreptapi.SRRemoveRestorePoint
title: SRRemoveRestorePoint function (srrestoreptapi.h)
author: windows-sdk-content
description: Deletes the specified restore point.
old-location: sr\srremoverestorepoint.htm
tech.root: sr
ms.assetid: e0f27947-7d88-4d15-8a92-85f88c3b60d4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SRRemoveRestorePoint, SRRemoveRestorePoint function [System Restore], _sr_srremoverestorepoint, sr.srremoverestorepoint, srrestoreptapi/SRRemoveRestorePoint
ms.topic: function
req.header: srrestoreptapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: SrClient.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - SrClient.dll
api_name:
 - SRRemoveRestorePoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SRRemoveRestorePoint function


## -description


Deletes the specified restore point.


## -parameters




### -param dwRPNum [in]

The sequence number of the restore point.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the specified restore point does not exist or cannot be removed, the return value is ERROR_INVALID_DATA. All other error codes indicate an internal error.




## -remarks



Applications should not call System Restore functions using load-time dynamic linking. Instead, use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> function to load SrClient.dll and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to call the function.




## -see-also




<a href="https://msdn.microsoft.com/46f0094d-9079-41b5-9efc-ef07082653d3">SRSetRestorePoint</a>
 

 


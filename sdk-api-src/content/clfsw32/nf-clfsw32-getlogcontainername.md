---
UID: NF:clfsw32.GetLogContainerName
title: GetLogContainerName function (clfsw32.h)
description: Retrieves the full path name of the specified container.
helpviewer_keywords: ["GetLogContainerName","GetLogContainerName function [Files]","clfsw32/GetLogContainerName","fs.getlogcontainername"]
old-location: fs\getlogcontainername.htm
tech.root: fs
ms.assetid: 4ff12544-797d-48b9-9c42-4bec059e6551
ms.date: 12/05/2018
ms.keywords: GetLogContainerName, GetLogContainerName function [Files], clfsw32/GetLogContainerName, fs.getlogcontainername
req.header: clfsw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetLogContainerName
 - clfsw32/GetLogContainerName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - GetLogContainerName
---

# GetLogContainerName function


## -description

Retrieves 
   the full path name of the specified container.  This function is 
   used mainly to obtain the full path name of a container referenced in the 
   <a href="/windows/desktop/api/clfs/ns-clfs-cls_container_information">CLFS_CONTAINER_INFORMATION</a> structure that is 
   returned in calls to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-scanlogcontainers">ScanLogContainers</a>.

## -parameters

### -param hLog [in]

A handle to the log that is obtained from a successful call to 
      <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>. 

The log handle could refer to a 
      log stream or a physical log.

### -param cidLogicalContainer [in]

The unique  identifier that is associated with a container.

### -param pwstrContainerName [in, out]

A pointer to a user-allocated buffer to receive the full path and name of the log container, in wide characters.

### -param cLenContainerName [in]

The size of the buffer pointed to by <i>pwstrContainerName</i>, in characters.

### -param pcActualLenContainerName [in, out, optional]

A pointer to a variable to receive the actual character count of the full container path name that is retrieved. 
      

If the function succeeds, the value of this parameter is less than or equal to 
      <i>cLenContainerName</i>. If the buffer is not large enough to store the whole container 
      path name, the function fails with <b>ERROR_MORE_DATA</b> and sets this parameter to the 
      size that is required for the full path name. For other failures the value is not defined.

## -returns

If the function succeeds, the return value is nonzero. 
      

If the function fails, the return value is zero (0). To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_container_information">CLFS_CONTAINER_INFORMATION</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-scanlogcontainers">ScanLogContainers</a>
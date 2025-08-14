---
UID: NF:fileapi.AreShortNamesEnabled
tech.root: fs
title: AreShortNamesEnabled function (fileapi.h)
ms.date: 01/05/2023
targetos: Windows
description: The AreShortNamesEnabled function determines whether short names are enabled for the specified volume.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: fileapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - fileapi.h
api_name:
 - AreShortNamesEnabled
f1_keywords:
 - AreShortNamesEnabled
 - fileapi/AreShortNamesEnabled
dev_langs:
 - c++
helpviewer_keywords:
 - AreShortNamesEnabled
---

## -description

The `AreShortNamesEnabled` function determines whether short names are enabled for the specified volume. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

## -parameters

### -param Handle

The handle to the volume or the handle to a file or directory that resides on the volume to query.

### -param Enabled

A pointer to a `BOOLEAN` value that receives the result of the query. If `TRUE`, short names are enabled for the volume, otherwise `FALSE` is returned.

## -returns

A `BOOLEAN` value that indicates whether the function succeeded. If the function succeeds, the return value is `TRUE`. If the function fails, the return value is `FALSE`. To get extended error information, call the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.

## -remarks

## -see-also

[Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file)

---
UID: NE:fileapi.DIRECTORY_FLAGS
tech.root: fs
title: DIRECTORY_FLAGS enumeration (fileapi.h)
ms.date: 04/10/2025
targetos: Windows
description: Defines the flags that can be used with the CreateDirectory2 function to specify how the directory should be created.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: fileapi.h
req.include-header: Windows.h
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11 24H2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2025 [desktop apps \| UWP apps]
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - fileapi.h
api_name:
 - DIRECTORY_FLAGS
f1_keywords:
 - DIRECTORY_FLAGS
 - fileapi/DIRECTORY_FLAGS
dev_langs:
 - c++
helpviewer_keywords:
 - DIRECTORY_FLAGS
---

## -description

The `DIRECTORY_FLAGS` enumeration defines the flags that can be used with the [CreateDirectory2](nf-fileapi-createdirectory2a.md) function to specify how the directory should be created.

## -enum-fields

### -field DIRECTORY_FLAGS_NONE

Indicates that no flags are set.

### -field DIRECTORY_FLAGS_DISALLOW_PATH_REDIRECTS

Prevent specified path name from being redirected by reparse points or symbolic links.

## -remarks

## -see-also

[CreateDirectory2a](nf-fileapi-createdirectory2a.md)

[CreateDirectory2w](nf-fileapi-createdirectory2w.md)

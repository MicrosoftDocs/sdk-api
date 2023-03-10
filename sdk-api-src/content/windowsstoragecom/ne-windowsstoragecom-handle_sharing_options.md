---
UID: NE:windowsstoragecom.HANDLE_SHARING_OPTIONS
title: HANDLE_SHARING_OPTIONS (windowsstoragecom.h)
description: Defines the requested sharing mode of the file handle.
helpviewer_keywords: ["HANDLE_SHARING_OPTIONS","HANDLE_SHARING_OPTIONS enumeration [Windows Runtime]","HSO_SHARE_DELETE","HSO_SHARE_NONE","HSO_SHARE_READ","HSO_SHARE_WRITE","windowsstoragecom/HANDLE_SHARING_OPTIONS","windowsstoragecom/HSO_SHARE_DELETE","windowsstoragecom/HSO_SHARE_NONE","windowsstoragecom/HSO_SHARE_READ","windowsstoragecom/HSO_SHARE_WRITE","winrt.handle_sharing_options"]
old-location: winrt\handle_sharing_options.htm
tech.root: WinRT
ms.assetid: 2CF1B6A9-6B6F-4413-8D76-B2F7A9D6D02E
ms.date: 12/05/2018
ms.keywords: HANDLE_SHARING_OPTIONS, HANDLE_SHARING_OPTIONS enumeration [Windows Runtime], HSO_SHARE_DELETE, HSO_SHARE_NONE, HSO_SHARE_READ, HSO_SHARE_WRITE, windowsstoragecom/HANDLE_SHARING_OPTIONS, windowsstoragecom/HSO_SHARE_DELETE, windowsstoragecom/HSO_SHARE_NONE, windowsstoragecom/HSO_SHARE_READ, windowsstoragecom/HSO_SHARE_WRITE, winrt.handle_sharing_options
req.header: windowsstoragecom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
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
req.typenames: HANDLE_SHARING_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HANDLE_SHARING_OPTIONS
 - windowsstoragecom/HANDLE_SHARING_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - windowsstoragecom.h
api_name:
 - HANDLE_SHARING_OPTIONS
---

# HANDLE_SHARING_OPTIONS enumeration


## -description

Defines the requested sharing mode of the file handle.

## -enum-fields

### -field HSO_SHARE_NONE:0

Prevents other processes from opening a file if they request delete, read, or write access.

### -field HSO_SHARE_READ:0x1

Enables subsequent open operations on a file to request read access.
Otherwise, other processes cannot open the file if they request read access.

### -field HSO_SHARE_WRITE:0x2

Enables subsequent open operations on a file to request write access.
Otherwise, other processes cannot open the file if they request write access.

### -field HSO_SHARE_DELETE:0x4

Enables subsequent open operations on a file to request delete access.
Otherwise, other processes cannot open the file if they request delete access.


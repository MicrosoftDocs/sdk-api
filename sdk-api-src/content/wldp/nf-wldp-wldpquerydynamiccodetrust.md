---
UID: NF:wldp.WldpQueryDynamicCodeTrust
tech.root: security
title: WldpQueryDynamicCodeTrust
ms.date: 08/23/2022
targetos: Windows
description: Retrieves a value that determines if the specified in-memory or on-disk .NET CRL dynamic code is trusted by Device Guard policy.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: wldp.dll
req.header: wldp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: wldp.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - wldp.dll
api_name:
 - WldpQueryDynamicCodeTrust
f1_keywords:
 - WldpQueryDynamicCodeTrust
 - wldp/WldpQueryDynamicCodeTrust
dev_langs:
 - c++
helpviewer_keywords:
 - WldpQueryDynamicCodeTrust
---

## -description

Retrieves a value that determines if the specified in-memory or on-disk .NET CRL dynamic code is trusted by Device Guard policy.

## -parameters

### -param fileHandle

Handle to the on-disk dynamic code file to check. If *fileHandle* is non-**NULL**, *baseImage* should be **NULL**.

### -param baseImage

Pointer to the in-memory PE file to check. If *baseImage* is non-**NULL**, *FileHandle* should be **NULL**.

### -param imageSize

When *baseImage* is non-**NULL**, indicates the buffer size that *baseImage* points to.

## -returns

This method returns **S\_OK** if successful or a failure code otherwise.

## -remarks

## -see-also


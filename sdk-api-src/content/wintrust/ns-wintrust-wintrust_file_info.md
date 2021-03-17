---
UID: NS:wintrust.WINTRUST_FILE_INFO_
title: WINTRUST_FILE_INFO (wintrust.h)
description: The WINTRUST_FILE_INFO structure is used when calling WinVerifyTrust to verify an individual file.
helpviewer_keywords: ["*PWINTRUST_FILE_INFO","PWINTRUCT_FILE_INFO","PWINTRUCT_FILE_INFO structure pointer [Security]","WINTRUST_FILE_INFO","WINTRUST_FILE_INFO structure [Security]","_win32_wintrust_file_info","security.wintrust_file_info","wintrust/PWINTRUCT_FILE_INFO","wintrust/WINTRUST_FILE_INFO"]
old-location: security\wintrust_file_info.htm
tech.root: security
ms.assetid: 3c3bef86-a2ed-47d1-a726-90630433358a
ms.date: 12/05/2018
ms.keywords: '*PWINTRUST_FILE_INFO, PWINTRUCT_FILE_INFO, PWINTRUCT_FILE_INFO structure pointer [Security], WINTRUST_FILE_INFO, WINTRUST_FILE_INFO structure [Security], _win32_wintrust_file_info, security.wintrust_file_info, wintrust/PWINTRUCT_FILE_INFO, wintrust/WINTRUST_FILE_INFO'
req.header: wintrust.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: WINTRUST_FILE_INFO, *PWINTRUST_FILE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WINTRUST_FILE_INFO_
 - wintrust/WINTRUST_FILE_INFO_
 - PWINTRUST_FILE_INFO
 - wintrust/PWINTRUST_FILE_INFO
 - WINTRUST_FILE_INFO
 - wintrust/WINTRUST_FILE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - WINTRUST_FILE_INFO
---

# WINTRUST_FILE_INFO structure


## -description

The <b>WINTRUST_FILE_INFO</b> structure is used when calling 
<a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> to verify an individual file.

## -struct-fields

### -field cbStruct

Count of bytes in this structure.

### -field pcwszFilePath

Full path and file name of the file to be verified. This parameter cannot be <b>NULL</b>.

### -field hFile

Optional. File handle to the open file to be verified. This handle must be to a file that has at least read permission. This member can be set to <b>NULL</b>.

### -field pgKnownSubject

Optional. Pointer to a <a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that specifies the subject type. This member can be set to <b>NULL</b>.
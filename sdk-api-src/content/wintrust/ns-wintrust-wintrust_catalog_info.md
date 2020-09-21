---
UID: NS:wintrust.WINTRUST_CATALOG_INFO_
title: WINTRUST_CATALOG_INFO (wintrust.h)
description: The WINTRUST_CATALOG_INFO structure is used when calling WinVerifyTrust to verify a member of a Microsoft catalog.
helpviewer_keywords: ["*PWINTRUST_CATALOG_INFO","PWINTRUST_CATALOG_INFO","PWINTRUST_CATALOG_INFO structure pointer [Security]","WINTRUST_CATALOG_INFO","WINTRUST_CATALOG_INFO structure [Security]","_win32_wintrust_catalog_info","security.wintrust_catalog_info","wintrust/PWINTRUST_CATALOG_INFO","wintrust/WINTRUST_CATALOG_INFO"]
old-location: security\wintrust_catalog_info.htm
tech.root: security
ms.assetid: 5d095e0f-c8c9-4717-b23a-985737b78431
ms.date: 12/05/2018
ms.keywords: '*PWINTRUST_CATALOG_INFO, PWINTRUST_CATALOG_INFO, PWINTRUST_CATALOG_INFO structure pointer [Security], WINTRUST_CATALOG_INFO, WINTRUST_CATALOG_INFO structure [Security], _win32_wintrust_catalog_info, security.wintrust_catalog_info, wintrust/PWINTRUST_CATALOG_INFO, wintrust/WINTRUST_CATALOG_INFO'
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
req.typenames: WINTRUST_CATALOG_INFO, *PWINTRUST_CATALOG_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WINTRUST_CATALOG_INFO_
 - wintrust/WINTRUST_CATALOG_INFO_
 - PWINTRUST_CATALOG_INFO
 - wintrust/PWINTRUST_CATALOG_INFO
 - WINTRUST_CATALOG_INFO
 - wintrust/WINTRUST_CATALOG_INFO
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
 - WINTRUST_CATALOG_INFO
---

# WINTRUST_CATALOG_INFO structure


## -description

The <b>WINTRUST_CATALOG_INFO</b> structure is used when calling 
<a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> to verify a member of a Microsoft catalog.

## -struct-fields

### -field cbStruct

Size, in bytes, of this structure.

### -field dwCatalogVersion

Optional. Catalog version number.

### -field pcwszCatalogFilePath

The full path and file name of the catalog file that contains the member to be verified.

### -field pcwszMemberTag

Tag of a member file to be verified.

### -field pcwszMemberFilePath

The full path and file name of the catalog member file to be verified.

### -field hMemberFile

Optional. Handle of the open catalog member file to be verified. The handle must be to a file with at least read permissions.

### -field pbCalculatedFileHash

Optional. The calculated hash of the file that contains the file to be verified.

### -field cbCalculatedFileHash

The size, in bytes, of the value passed in the <b>pbCalculatedFileHash</b> member. <b>cbCalculatedFileHash</b> is used only if the calculated hash is being passed.

### -field pcCatalogContext

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure that represents  a catalog context to be used instead of a catalog file.

### -field hCatAdmin

Handle to the catalog administrator context that was used when calculating the hash of the file. This value can be zero only for a SHA1 file hash.<b>Windows 8 and Windows Server 2012:  </b>Support for this member begins.
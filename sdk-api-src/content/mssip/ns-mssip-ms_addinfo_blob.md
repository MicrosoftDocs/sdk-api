---
UID: NS:mssip.MS_ADDINFO_BLOB_
title: MS_ADDINFO_BLOB (mssip.h)
description: Provides additional information for in-memory BLOB subject types.
helpviewer_keywords: ["*PMS_ADDINFO_BLOB","MS_ADDINFO_BLOB","MS_ADDINFO_BLOB structure [Security]","PMS_ADDINFO_BLOB","PMS_ADDINFO_BLOB structure pointer [Security]","mssip/MS_ADDINFO_BLOB","mssip/PMS_ADDINFO_BLOB","security.ms_addinfo_blob"]
old-location: security\ms_addinfo_blob.htm
tech.root: security
ms.assetid: 236c8778-0b80-4157-8a81-24712ebf9a77
ms.date: 12/05/2018
ms.keywords: '*PMS_ADDINFO_BLOB, MS_ADDINFO_BLOB, MS_ADDINFO_BLOB structure [Security], PMS_ADDINFO_BLOB, PMS_ADDINFO_BLOB structure pointer [Security], mssip/MS_ADDINFO_BLOB, mssip/PMS_ADDINFO_BLOB, security.ms_addinfo_blob'
req.header: mssip.h
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
req.typenames: MS_ADDINFO_BLOB, *PMS_ADDINFO_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MS_ADDINFO_BLOB_
 - mssip/MS_ADDINFO_BLOB_
 - PMS_ADDINFO_BLOB
 - mssip/PMS_ADDINFO_BLOB
 - MS_ADDINFO_BLOB
 - mssip/MS_ADDINFO_BLOB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mssip.h
api_name:
 - MS_ADDINFO_BLOB
---

# MS_ADDINFO_BLOB structure


## -description

The <b>MS_ADDINFO_BLOB</b> structure provides additional information for in-memory <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> subject types.

## -struct-fields

### -field cbStruct

The size, in bytes, of this structure.

### -field cbMemObject

The size, in bytes, of the data in the <i>pbMemObject</i> member.

### -field pbMemObject

A pointer to the in-memory BLOB subject.

### -field cbMemSignedMsg

The size, in bytes, of the data in the <i>pbMemSignedMsg</i> member.

### -field pbMemSignedMsg

A pointer to the signed message.
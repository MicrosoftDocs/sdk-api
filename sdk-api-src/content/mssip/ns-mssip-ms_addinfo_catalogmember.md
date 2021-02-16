---
UID: NS:mssip.MS_ADDINFO_CATALOGMEMBER_
title: MS_ADDINFO_CATALOGMEMBER (mssip.h)
description: Provides additional information for catalog member subject types.
helpviewer_keywords: ["*PMS_ADDINFO_CATALOGMEMBER","MS_ADDINFO_CATALOGMEMBER","MS_ADDINFO_CATALOGMEMBER structure [Security]","PMS_ADDINFO_CATALOGMEMBER","PMS_ADDINFO_CATALOGMEMBER structure pointer [Security]","mssip/MS_ADDINFO_CATALOGMEMBER_","mssip/PMS_ADDINFO_CATALOGMEMBER","security.ms_addinfo_catalogmember"]
old-location: security\ms_addinfo_catalogmember.htm
tech.root: security
ms.assetid: 40a00c8a-95e4-406c-b04e-0d29beb70d67
ms.date: 12/05/2018
ms.keywords: '*PMS_ADDINFO_CATALOGMEMBER, MS_ADDINFO_CATALOGMEMBER, MS_ADDINFO_CATALOGMEMBER structure [Security], PMS_ADDINFO_CATALOGMEMBER, PMS_ADDINFO_CATALOGMEMBER structure pointer [Security], mssip/MS_ADDINFO_CATALOGMEMBER_, mssip/PMS_ADDINFO_CATALOGMEMBER, security.ms_addinfo_catalogmember'
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
req.typenames: MS_ADDINFO_CATALOGMEMBER, *PMS_ADDINFO_CATALOGMEMBER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MS_ADDINFO_CATALOGMEMBER_
 - mssip/MS_ADDINFO_CATALOGMEMBER_
 - PMS_ADDINFO_CATALOGMEMBER
 - mssip/PMS_ADDINFO_CATALOGMEMBER
 - MS_ADDINFO_CATALOGMEMBER
 - mssip/MS_ADDINFO_CATALOGMEMBER
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
 - MS_ADDINFO_CATALOGMEMBER
---

# MS_ADDINFO_CATALOGMEMBER structure


## -description

The <b>MS_ADDINFO_CATALOGMEMBER</b> structure provides additional information for catalog member subject types.

## -struct-fields

### -field cbStruct

The size, in bytes, of this structure.

### -field pStore

A [CRYPTCATSTORE](/windows/desktop/api/mscat/ns-mscat-cryptcatstore) structure that contains a catalog file store.

### -field pMember

A [CRYPTCATMEMBER](/windows/desktop/api/mscat/ns-mscat-cryptcatmember) structure that contains a catalog member.
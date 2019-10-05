---
UID: NS:mssip.MS_ADDINFO_CATALOGMEMBER_
title: MS_ADDINFO_CATALOGMEMBER (mssip.h)
author: windows-sdk-content
description: Provides additional information for catalog member subject types.
old-location: security\ms_addinfo_catalogmember.htm
tech.root: SecCrypto
ms.assetid: 40a00c8a-95e4-406c-b04e-0d29beb70d67
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PMS_ADDINFO_CATALOGMEMBER, MS_ADDINFO_CATALOGMEMBER, MS_ADDINFO_CATALOGMEMBER structure [Security], PMS_ADDINFO_CATALOGMEMBER, PMS_ADDINFO_CATALOGMEMBER structure pointer [Security], mssip/MS_ADDINFO_CATALOGMEMBER_, mssip/PMS_ADDINFO_CATALOGMEMBER, security.ms_addinfo_catalogmember"
ms.topic: struct
f1_keywords: 
 - "mssip/MS_ADDINFO_CATALOGMEMBER"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mssip.h
api_name:
 - MS_ADDINFO_CATALOGMEMBER
targetos: Windows
req.typenames: MS_ADDINFO_CATALOGMEMBER, *PMS_ADDINFO_CATALOGMEMBER
req.redist: 
ms.custom: 19H1
---

# MS_ADDINFO_CATALOGMEMBER structure


## -description


The <b>MS_ADDINFO_CATALOGMEMBER</b> structure provides additional information for catalog member subject types.


## -struct-fields




### -field cbStruct

The size, in bytes, of this structure.


### -field pStore

A <a href="https://docs.microsoft.com/windows/desktop/api/mscat/ns-mscat-cryptcatstore_">CRYPTCATSTORE</a> structure that contains a catalog file store.


### -field pMember

A <a href="https://docs.microsoft.com/windows/desktop/api/mscat/ns-mscat-cryptcatmember_">CRYPTCATMEMBER</a> structure that contains a catalog member.


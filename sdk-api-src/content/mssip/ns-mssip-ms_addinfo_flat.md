---
UID: NS:mssip.MS_ADDINFO_FLAT_
title: MS_ADDINFO_FLAT (mssip.h)
description: Provides additional information about flat or end-to-end subject types.
helpviewer_keywords: ["*PMS_ADDINFO_FLAT","MS_ADDINFO_FLAT","MS_ADDINFO_FLAT structure [Security]","PMS_ADDINFO_FLAT","PMS_ADDINFO_FLAT structure pointer [Security]","mssip/MS_ADDINFO_FLAT_","mssip/PMS_ADDINFO_FLAT","security.ms_addinfo_flat"]
old-location: security\ms_addinfo_flat.htm
tech.root: security
ms.assetid: 9f5bebd1-8eda-456d-9339-3334a19c0ea4
ms.date: 12/05/2018
ms.keywords: '*PMS_ADDINFO_FLAT, MS_ADDINFO_FLAT, MS_ADDINFO_FLAT structure [Security], PMS_ADDINFO_FLAT, PMS_ADDINFO_FLAT structure pointer [Security], mssip/MS_ADDINFO_FLAT_, mssip/PMS_ADDINFO_FLAT, security.ms_addinfo_flat'
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
req.typenames: MS_ADDINFO_FLAT, *PMS_ADDINFO_FLAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MS_ADDINFO_FLAT_
 - mssip/MS_ADDINFO_FLAT_
 - PMS_ADDINFO_FLAT
 - mssip/PMS_ADDINFO_FLAT
 - MS_ADDINFO_FLAT
 - mssip/MS_ADDINFO_FLAT
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
 - MS_ADDINFO_FLAT
---

# MS_ADDINFO_FLAT structure


## -description

The <b>MS_ADDINFO_FLAT</b> structure provides additional information about flat or end-to-end subject types.

## -struct-fields

### -field cbStruct

The size, in bytes, of this structure.

### -field pIndirectData

A [SIP_INDIRECT_DATA](/windows/desktop/api/mssip/ns-mssip-sip_indirect_data) structure that contains the <a href="/windows/desktop/SecGloss/h-gly">hash</a> of a flat file subject.
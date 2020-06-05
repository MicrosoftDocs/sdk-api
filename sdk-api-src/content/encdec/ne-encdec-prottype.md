---
UID: NE:encdec.ProtType
title: ProtType (encdec.h)
description: This topic applies to Windows XP Service Pack 1 or later.helpviewer_keywords: ["PROT_COPY_BF","PROT_COPY_CN_RECORDING_STOP","PROT_COPY_FREE","PROT_COPY_FREE_CIT","PROT_COPY_FREE_SECURE","PROT_COPY_INVALID","PROT_COPY_NEVER","PROT_COPY_NEVER_REALLY","PROT_COPY_NO_MORE","PROT_COPY_ONCE","ProtType","ProtType enumeration [Microsoft TV Technologies]","encdec/PROT_COPY_BF","encdec/PROT_COPY_CN_RECORDING_STOP","encdec/PROT_COPY_FREE","encdec/PROT_COPY_FREE_CIT","encdec/PROT_COPY_FREE_SECURE","encdec/PROT_COPY_INVALID","encdec/PROT_COPY_NEVER","encdec/PROT_COPY_NEVER_REALLY","encdec/PROT_COPY_NO_MORE","encdec/PROT_COPY_ONCE","encdec/ProtType","mstv.prottype"]
old-location: mstv\prottype.htm
tech.root: mstv
ms.assetid: 190b8483-91c8-4fe4-8189-637749393151
ms.date: 12/05/2018
ms.keywords: PROT_COPY_BF, PROT_COPY_CN_RECORDING_STOP, PROT_COPY_FREE, PROT_COPY_FREE_CIT, PROT_COPY_FREE_SECURE, PROT_COPY_INVALID, PROT_COPY_NEVER, PROT_COPY_NEVER_REALLY, PROT_COPY_NO_MORE, PROT_COPY_ONCE, ProtType, ProtType enumeration [Microsoft TV Technologies], encdec/PROT_COPY_BF, encdec/PROT_COPY_CN_RECORDING_STOP, encdec/PROT_COPY_FREE, encdec/PROT_COPY_FREE_CIT, encdec/PROT_COPY_FREE_SECURE, encdec/PROT_COPY_INVALID, encdec/PROT_COPY_NEVER, encdec/PROT_COPY_NEVER_REALLY, encdec/PROT_COPY_NO_MORE, encdec/PROT_COPY_ONCE, encdec/ProtType, mstv.prottype
f1_keywords:
- encdec/ProtType
dev_langs:
- c++
req.header: encdec.h
req.include-header: Tvratings.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
- encdec.h
api_name:
- ProtType
targetos: Windows
req.typenames: ProtType
req.redist: 
ms.custom: 19H1
---

# ProtType enumeration


## -description



This topic applies to Windows XP Service Pack 1 or later.
        



The <b>ProtType</b> enumeration type specifies various types of content protection.


## -enum-fields




### -field PROT_COPY_FREE

Copy Free.


### -field PROT_COPY_ONCE

Copy Once.


### -field PROT_COPY_NEVER

Copy Never.


### -field PROT_COPY_NEVER_REALLY

Reserved.


### -field PROT_COPY_NO_MORE

Copy No More.


### -field PROT_COPY_FREE_CIT

The Copy Control Information (CCI) flag indicates Copy Free, but the Constrained Image Trigger (CIT) bit is set. The content is encrypted.


### -field PROT_COPY_BF

Reserved.


### -field PROT_COPY_CN_RECORDING_STOP

Reserved.


### -field PROT_COPY_FREE_SECURE

The Copy Control Information (CCI) flag indicates Copy Free, but the Redistribution Control Trigger (RCT) bit is set. The content is encrypted.


### -field PROT_COPY_INVALID

Error or invalid protection scheme. Treat as Copy Never.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/ne-tvratings-entvrat_genericlevel">EnTvRat_GenericLevel</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tv-ratings-enumerations">TV Ratings Enumerations</a>
 

 


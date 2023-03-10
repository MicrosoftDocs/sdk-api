---
UID: NE:sbtsv._TS_SB_SORT_BY
title: TS_SB_SORT_BY (sbtsv.h)
description: Specifies sort order. It is used as a parameter in the EnumerateTargets method.
helpviewer_keywords: ["TS_SB_SORT_BY","TS_SB_SORT_BY enumeration [Remote Desktop Services]","TS_SB_SORT_BY_NAME","TS_SB_SORT_BY_NONE","TS_SB_SORT_BY_PROP","sbtsv/TS_SB_SORT_BY","sbtsv/TS_SB_SORT_BY_NAME","sbtsv/TS_SB_SORT_BY_NONE","sbtsv/TS_SB_SORT_BY_PROP","termserv.ts_sb_sort_by"]
old-location: termserv\ts_sb_sort_by.htm
tech.root: TermServ
ms.assetid: 50945048-5E79-4423-8983-543085E3D953
ms.date: 12/05/2018
ms.keywords: TS_SB_SORT_BY, TS_SB_SORT_BY enumeration [Remote Desktop Services], TS_SB_SORT_BY_NAME, TS_SB_SORT_BY_NONE, TS_SB_SORT_BY_PROP, sbtsv/TS_SB_SORT_BY, sbtsv/TS_SB_SORT_BY_NAME, sbtsv/TS_SB_SORT_BY_NONE, sbtsv/TS_SB_SORT_BY_PROP, termserv.ts_sb_sort_by
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TS_SB_SORT_BY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TS_SB_SORT_BY
 - sbtsv/_TS_SB_SORT_BY
 - TS_SB_SORT_BY
 - sbtsv/TS_SB_SORT_BY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - sbtsv.h
api_name:
 - TS_SB_SORT_BY
---

# TS_SB_SORT_BY enumeration


## -description

Specifies sort order. It is used as a parameter in the <a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets">EnumerateTargets</a> method.

## -enum-fields

### -field TS_SB_SORT_BY_NONE:0

Do not sort.

### -field TS_SB_SORT_BY_NAME:0x1

Sort by target name.

### -field TS_SB_SORT_BY_PROP:0x2

Sort by a specified property.

## -see-also

<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets">EnumerateTargets</a>

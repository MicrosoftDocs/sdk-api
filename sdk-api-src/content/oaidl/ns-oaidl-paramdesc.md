---
UID: NS:oaidl.tagPARAMDESC
title: PARAMDESC (oaidl.h)
description: Contains information needed for transferring a structure element, parameter, or function return value between processes.
helpviewer_keywords: ["*LPPARAMDESC","LPPARAMDESC","LPPARAMDESC structure pointer [Automation]","PARAMDESC","PARAMDESC structure [Automation]","_oa96_PARAMDESC","automat.paramdesc","oaidl/LPPARAMDESC","oaidl/PARAMDESC"]
old-location: automat\paramdesc.htm
tech.root: automat
ms.assetid: 3b3b2c54-1997-4d1f-9934-81621500b2b9
ms.date: 12/05/2018
ms.keywords: '*LPPARAMDESC, LPPARAMDESC, LPPARAMDESC structure pointer [Automation], PARAMDESC, PARAMDESC structure [Automation], _oa96_PARAMDESC, automat.paramdesc, oaidl/LPPARAMDESC, oaidl/PARAMDESC'
req.header: oaidl.h
req.include-header: 
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
targetos: Windows
req.typenames: PARAMDESC, *LPPARAMDESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPARAMDESC
 - oaidl/tagPARAMDESC
 - LPPARAMDESC
 - oaidl/LPPARAMDESC
 - PARAMDESC
 - oaidl/PARAMDESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OaIdl.h
api_name:
 - PARAMDESC
---

# PARAMDESC structure


## -description

Contains information needed for transferring a structure element, parameter, or function return value between processes.

## -struct-fields

### -field pparamdescex

The default value for the parameter, if PARAMFLAG_FHASDEFAULT is specified in <b>wParamFlags</b>.

### -field wParamFlags

The parameter flags. See <a href="/previous-versions/windows/desktop/automat/paramflags">PARAMFLAG Constants</a>.
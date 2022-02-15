---
UID: NE:objidlbase._THDTYPE
title: THDTYPE (objidlbase.h)
description: Indicates whether a particular thread supports a message loop.
helpviewer_keywords: ["THDTYPE","THDTYPE enumeration [COM]","THDTYPE_BLOCKMESSAGES","THDTYPE_PROCESSMESSAGES","_com_THDTYPE","com.thdtype","objidlbase/THDTYPE","objidlbase/THDTYPE_BLOCKMESSAGES","objidlbase/THDTYPE_PROCESSMESSAGES"]
old-location: com\thdtype.htm
tech.root: com
ms.assetid: c1f9ab7b-8915-4433-ae9f-57b1aedcad4d
ms.date: 12/05/2018
ms.keywords: THDTYPE, THDTYPE enumeration [COM], THDTYPE_BLOCKMESSAGES, THDTYPE_PROCESSMESSAGES, _com_THDTYPE, com.thdtype, objidlbase/THDTYPE, objidlbase/THDTYPE_BLOCKMESSAGES, objidlbase/THDTYPE_PROCESSMESSAGES
req.header: objidlbase.h
req.include-header: Objidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: THDTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _THDTYPE
 - objidlbase/_THDTYPE
 - THDTYPE
 - objidlbase/THDTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - THDTYPE
---

# THDTYPE enumeration


## -description

Indicates whether a particular thread supports a message loop.

## -enum-fields

### -field THDTYPE_BLOCKMESSAGES:0

The thread does not support a message loop. This behavior is associated with multithreaded apartments.

### -field THDTYPE_PROCESSMESSAGES:1

The thread supports a message loop. This behavior is associated with single-threaded apartments.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-icomthreadinginfo-getcurrentthreadtype">IComThreadingInfo::GetCurrentThreadType</a>

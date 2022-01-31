---
UID: NE:callobj.CALLFRAME_WALK
title: CALLFRAME_WALK (callobj.h)
description: Determines the parameter type to be walked.
helpviewer_keywords: ["CALLFRAME_WALK","CALLFRAME_WALK enumeration [COM]","CALLFRAME_WALK_IN","CALLFRAME_WALK_INOUT","CALLFRAME_WALK_OUT","_com_CALLFRAME_WALK","callobj/CALLFRAME_WALK","callobj/CALLFRAME_WALK_IN","callobj/CALLFRAME_WALK_INOUT","callobj/CALLFRAME_WALK_OUT","com.callframe_walk"]
old-location: com\callframe_walk.htm
tech.root: com
ms.assetid: 52327707-43b0-4041-8fa1-62a9a62dc6b7
ms.date: 12/05/2018
ms.keywords: CALLFRAME_WALK, CALLFRAME_WALK enumeration [COM], CALLFRAME_WALK_IN, CALLFRAME_WALK_INOUT, CALLFRAME_WALK_OUT, _com_CALLFRAME_WALK, callobj/CALLFRAME_WALK, callobj/CALLFRAME_WALK_IN, callobj/CALLFRAME_WALK_INOUT, callobj/CALLFRAME_WALK_OUT, com.callframe_walk
req.header: callobj.h
req.include-header: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CALLFRAME_WALK
 - callobj/CALLFRAME_WALK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CallObj.h
api_name:
 - CALLFRAME_WALK
---

# CALLFRAME_WALK enumeration


## -description

Determines the parameter type to be walked.

## -enum-fields

### -field CALLFRAME_WALK_IN:1

The [in] parameter values will be walked.

### -field CALLFRAME_WALK_INOUT:2

The [in, out] parameter values will be walked.

### -field CALLFRAME_WALK_OUT:4

The [out] parameter values will be walked.

## -see-also

<a href="/windows/desktop/api/callobj/nf-callobj-icallframe-walkframe">ICallFrame::WalkFrame</a>

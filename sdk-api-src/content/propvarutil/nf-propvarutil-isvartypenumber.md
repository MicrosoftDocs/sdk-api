---
UID: NF:propvarutil.IsVarTypeNumber
title: IsVarTypeNumber function (propvarutil.h)
description: Specifies whether VARTYPE is a number.
helpviewer_keywords: ["IsVarTypeNumber","IsVarTypeNumber function [Windows Properties]","_shell_IsVarTypeNumber","properties.IsVarTypeNumber","propvarutil/IsVarTypeNumber","shell.IsVarTypeNumber"]
old-location: properties\IsVarTypeNumber.htm
tech.root: properties
ms.assetid: 57051571-4871-46dd-8319-9c9f29890603
ms.date: 12/05/2018
ms.keywords: IsVarTypeNumber, IsVarTypeNumber function [Windows Properties], _shell_IsVarTypeNumber, properties.IsVarTypeNumber, propvarutil/IsVarTypeNumber, shell.IsVarTypeNumber
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IsVarTypeNumber
 - propvarutil/IsVarTypeNumber
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propvarutil.h
api_name:
 - IsVarTypeNumber
---

# IsVarTypeNumber function


## -description

Specifies whether <a href="/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a> is a number.

## -parameters

### -param vt [in]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a></b>

Specifies the <a href="/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a> being queried.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if <a href="/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a> is a number.

## -remarks

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.
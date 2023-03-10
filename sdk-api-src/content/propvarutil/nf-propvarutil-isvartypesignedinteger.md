---
UID: NF:propvarutil.IsVarTypeSignedInteger
title: IsVarTypeSignedInteger function (propvarutil.h)
description: Returns whether a VARTYPE is a signed integer.
helpviewer_keywords: ["IsVarTypeSignedInteger","IsVarTypeSignedInteger function [Windows Properties]","_shell_IsVarTypeSignedInteger","properties.IsVarTypeSignedInteger","propvarutil/IsVarTypeSignedInteger","shell.IsVarTypeSignedInteger"]
old-location: properties\IsVarTypeSignedInteger.htm
tech.root: properties
ms.assetid: 8d5510c6-6c1c-4cc5-85a6-00514278029d
ms.date: 12/05/2018
ms.keywords: IsVarTypeSignedInteger, IsVarTypeSignedInteger function [Windows Properties], _shell_IsVarTypeSignedInteger, properties.IsVarTypeSignedInteger, propvarutil/IsVarTypeSignedInteger, shell.IsVarTypeSignedInteger
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
 - IsVarTypeSignedInteger
 - propvarutil/IsVarTypeSignedInteger
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
 - IsVarTypeSignedInteger
---

# IsVarTypeSignedInteger function


## -description

Returns whether a <a href="/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a> is a signed integer.

## -parameters

### -param vt [in]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a></b>

Specifies the <a href="/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a> being queried.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if <a href="/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a> is a signed integer; otherwise, <b>FALSE</b>.

## -remarks

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.
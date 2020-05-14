---
UID: NF:propvarutil.IsVarTypeUnsignedInteger
title: IsVarTypeUnsignedInteger function (propvarutil.h)
description: Returns whether a VARTYPE is an unsigned integer.helpviewer_keywords: ["IsVarTypeUnsignedInteger","IsVarTypeUnsignedInteger function [Windows Properties]","_shell_IsVarTypeUnsignedInteger","properties.IsVarTypeUnsignedInteger","propvarutil/IsVarTypeUnsignedInteger","shell.IsVarTypeUnsignedInteger"]
old-location: properties\IsVarTypeUnsignedInteger.htm
tech.root: properties
ms.assetid: e3af20d4-be61-446e-90be-765f1e84178a
ms.date: 12/05/2018
ms.keywords: IsVarTypeUnsignedInteger, IsVarTypeUnsignedInteger function [Windows Properties], _shell_IsVarTypeUnsignedInteger, properties.IsVarTypeUnsignedInteger, propvarutil/IsVarTypeUnsignedInteger, shell.IsVarTypeUnsignedInteger
f1_keywords:
- propvarutil/IsVarTypeUnsignedInteger
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Propvarutil.h
api_name:
- IsVarTypeUnsignedInteger
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# IsVarTypeUnsignedInteger function


## -description


Returns whether a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a> is an unsigned integer.


## -parameters




### -param vt [in]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a></b>

Specifies the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a> being queried.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms221127(v=vs.85)">VARTYPE</a> is an unsigned integer; otherwise, <b>FALSE</b>.




## -remarks



This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.




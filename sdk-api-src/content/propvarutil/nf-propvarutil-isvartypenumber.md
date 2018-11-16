---
UID: NF:propvarutil.IsVarTypeNumber
title: IsVarTypeNumber function
author: windows-sdk-content
description: Specifies whether VARTYPE is a number.
old-location: properties\IsVarTypeNumber.htm
tech.root: properties
ms.assetid: 57051571-4871-46dd-8319-9c9f29890603
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IsVarTypeNumber, IsVarTypeNumber function [Windows Properties], _shell_IsVarTypeNumber, properties.IsVarTypeNumber, propvarutil/IsVarTypeNumber, shell.IsVarTypeNumber
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - IsVarTypeNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- 
: 
- IsVarTypeNumber
: 
---

# IsVarTypeNumber function


## -description


Specifies whether <a href="https://msdn.microsoft.com/en-us/library/ms221127(v=VS.85).aspx">VARTYPE</a> is a number.


## -parameters




### -param vt [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms221127(v=VS.85).aspx">VARTYPE</a></b>

Specifies the <a href="https://msdn.microsoft.com/en-us/library/ms221127(v=VS.85).aspx">VARTYPE</a> being queried.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if <a href="https://msdn.microsoft.com/en-us/library/ms221127(v=VS.85).aspx">VARTYPE</a> is a number.




## -remarks



This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.




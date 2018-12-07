---
UID: NF:propvarutil.IsVarTypeFloat
title: IsVarTypeFloat function
author: windows-sdk-content
description: Returns whether a VARTYPE is a float.
old-location: properties\IsVarTypeFloat.htm
tech.root: properties
ms.assetid: ff233e26-c02b-47ca-958b-a5282b280ecd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IsVarTypeFloat, IsVarTypeFloat function [Windows Properties], _shell_IsVarTypeFloat, properties.IsVarTypeFloat, propvarutil/IsVarTypeFloat, shell.IsVarTypeFloat
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
 - IsVarTypeFloat
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IsVarTypeFloat function


## -description


Returns whether a <a href="https://msdn.microsoft.com/en-us/library/ms221127(v=VS.85).aspx">VARTYPE</a> is a float.


## -parameters




### -param vt [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms221127(v=VS.85).aspx">VARTYPE</a></b>

Specifies the <a href="https://msdn.microsoft.com/en-us/library/ms221127(v=VS.85).aspx">VARTYPE</a> being queried.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if <a href="https://msdn.microsoft.com/en-us/library/ms221127(v=VS.85).aspx">VARTYPE</a> is a float.




## -remarks



This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.




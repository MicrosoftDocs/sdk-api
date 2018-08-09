---
UID: NF:propvarutil.IsVarTypeInteger
title: IsVarTypeInteger function
author: windows-sdk-content
description: Returns whether a VARTYPE is an integer.
old-location: properties\IsVarTypeInteger.htm
old-project: properties
ms.assetid: 3e183355-8e71-4f6d-a348-c9dde9aa5953
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IsVarTypeInteger, IsVarTypeInteger function [Windows Properties], _shell_IsVarTypeInteger, properties.IsVarTypeInteger, propvarutil/IsVarTypeInteger, shell.IsVarTypeInteger
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propvarutil.h
api_name:
 - IsVarTypeInteger
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IsVarTypeInteger function


## -description


Returns whether a <a href="https://msdn.microsoft.com/en-us/library/ms221127(v=VS.85).aspx">VARTYPE</a> is an integer.


## -parameters




### -param vt [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms221127(v=VS.85).aspx">VARTYPE</a></b>

Specifies the <a href="https://msdn.microsoft.com/en-us/library/ms221127(v=VS.85).aspx">VARTYPE</a> being queried.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if <a href="https://msdn.microsoft.com/en-us/library/ms221127(v=VS.85).aspx">VARTYPE</a> is an integer.




## -remarks



This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.




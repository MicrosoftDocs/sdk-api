---
UID: NF:propvarutil.IsVarTypeSignedInteger
title: IsVarTypeSignedInteger function
author: windows-sdk-content
description: Returns whether a VARTYPE is a signed integer.
old-location: properties\IsVarTypeSignedInteger.htm
old-project: properties
ms.assetid: 8d5510c6-6c1c-4cc5-85a6-00514278029d
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IsVarTypeSignedInteger, IsVarTypeSignedInteger function [Windows Properties], _shell_IsVarTypeSignedInteger, properties.IsVarTypeSignedInteger, propvarutil/IsVarTypeSignedInteger, shell.IsVarTypeSignedInteger
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
 - IsVarTypeSignedInteger
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IsVarTypeSignedInteger function


## -description


Returns whether a <a href="317b911b-1805-402d-a9cb-159546bc88b4">VARTYPE</a> is a signed integer.


## -parameters




### -param vt [in]

Type: <b><a href="317b911b-1805-402d-a9cb-159546bc88b4">VARTYPE</a></b>

Specifies the <a href="317b911b-1805-402d-a9cb-159546bc88b4">VARTYPE</a> being queried.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if <a href="317b911b-1805-402d-a9cb-159546bc88b4">VARTYPE</a> is a signed integer; otherwise, <b>FALSE</b>.




## -remarks



This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.




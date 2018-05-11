---
UID: NF:propvarutil.IsVarTypeUnsignedInteger
title: IsVarTypeUnsignedInteger function
author: windows-driver-content
description: Returns whether a VARTYPE is an unsigned integer.
old-location: properties\IsVarTypeUnsignedInteger.htm
old-project: properties
ms.assetid: e3af20d4-be61-446e-90be-765f1e84178a
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IsVarTypeUnsignedInteger, IsVarTypeUnsignedInteger function [Windows Properties], _shell_IsVarTypeUnsignedInteger, properties.IsVarTypeUnsignedInteger, propvarutil/IsVarTypeUnsignedInteger, shell.IsVarTypeUnsignedInteger
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Propvarutil.h
api_name:
-	IsVarTypeUnsignedInteger
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IsVarTypeUnsignedInteger function


## -description


Returns whether a <a href="317b911b-1805-402d-a9cb-159546bc88b4">VARTYPE</a> is an unsigned integer.


## -parameters




### -param vt [in]

Type: <b><a href="317b911b-1805-402d-a9cb-159546bc88b4">VARTYPE</a></b>

Specifies the <a href="317b911b-1805-402d-a9cb-159546bc88b4">VARTYPE</a> being queried.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if <a href="317b911b-1805-402d-a9cb-159546bc88b4">VARTYPE</a> is an unsigned integer; otherwise, <b>FALSE</b>.




## -remarks



This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.




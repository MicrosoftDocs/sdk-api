---
UID: NF:dpa_dsa.DSA_GetSize
title: DSA_GetSize function
author: windows-driver-content
description: Gets the size of the dynamic structure array (DSA).
old-location: controls\DSA_GetSize.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_getsize.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: DSA_GetSize, DSA_GetSize function [Windows Controls], _shell_DSA_GetSize, _shell_DSA_GetSize_cpp, controls.DSA_GetSize, controls._shell_DSA_GetSize, dpa_dsa/DSA_GetSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dpa_dsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CRYPTPROTECT_PROMPTSTRUCT, *PCRYPTPROTECT_PROMPTSTRUCT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Comctl32.dll
api_name:
-	DSA_GetSize
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll
req.irql: 
---

# DSA_GetSize function


## -description


Gets the size of the dynamic structure array (DSA).


## -parameters




### -param hdsa [in]

Type: <b>HDSA</b>

A handle to an existing DSA.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONGLONG</a></b>

Returns the size of the DSA, including the internal bookkeeping information, in bytes. If <i>hdsa</i> is <b>NULL</b>, the function returns zero.




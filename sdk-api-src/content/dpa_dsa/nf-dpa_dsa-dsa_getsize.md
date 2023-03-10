---
UID: NF:dpa_dsa.DSA_GetSize
title: DSA_GetSize function (dpa_dsa.h)
description: Gets the size of the dynamic structure array (DSA).
helpviewer_keywords: ["DSA_GetSize","DSA_GetSize function [Windows Controls]","_shell_DSA_GetSize","_shell_DSA_GetSize_cpp","controls.DSA_GetSize","controls._shell_DSA_GetSize","dpa_dsa/DSA_GetSize"]
old-location: controls\DSA_GetSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_getsize.htm
ms.date: 12/05/2018
ms.keywords: DSA_GetSize, DSA_GetSize function [Windows Controls], _shell_DSA_GetSize, _shell_DSA_GetSize_cpp, controls.DSA_GetSize, controls._shell_DSA_GetSize, dpa_dsa/DSA_GetSize
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
req.lib: 
req.dll: Comctl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DSA_GetSize
 - dpa_dsa/DSA_GetSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DSA_GetSize
---

# DSA_GetSize function


## -description

Gets the size of the dynamic structure array (DSA).

## -parameters

### -param hdsa [in]

Type: <b>HDSA</b>

A handle to an existing DSA.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONGLONG</a></b>

Returns the size of the DSA, including the internal bookkeeping information, in bytes. If <i>hdsa</i> is <b>NULL</b>, the function returns zero.
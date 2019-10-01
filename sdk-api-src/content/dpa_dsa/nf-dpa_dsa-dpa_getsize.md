---
UID: NF:dpa_dsa.DPA_GetSize
title: DPA_GetSize function (dpa_dsa.h)
author: windows-sdk-content
description: Gets the size of a dynamic pointer array (DPA).
old-location: controls\DPA_GetSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_getsize.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DPA_GetSize, DPA_GetSize function [Windows Controls], _shell_DPA_GetSize, _shell_DPA_GetSize_cpp, controls.DPA_GetSize, controls._shell_DPA_GetSize, dpa_dsa/DPA_GetSize
ms.topic: function
f1_keywords: 
 - "dpa_dsa/DPA_GetSize"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DPA_GetSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DPA_GetSize function


## -description


Gets the size of a dynamic pointer array (DPA).


## -parameters




### -param hdpa [in]

Type: <b>HDPA</b>

A handle to an existing DPA.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">ULONGLONG</a></b>

Returns the size of the DPA, including the internal bookkeeping information. If <i>pdpa</i> is <b>NULL</b>, the function returns zero.




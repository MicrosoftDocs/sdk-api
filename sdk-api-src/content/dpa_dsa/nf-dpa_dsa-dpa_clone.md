---
UID: NF:dpa_dsa.DPA_Clone
title: DPA_Clone function
author: windows-sdk-content
description: Duplicates a dynamic pointer array (DPA).
old-location: controls\DPA_Clone.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_clone.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DPA_Clone, DPA_Clone function [Windows Controls], _shell_DPA_Clone, _shell_DPA_Clone_cpp, controls.DPA_Clone, controls._shell_DPA_Clone, dpa_dsa/DPA_Clone
ms.topic: function
req.header: dpa_dsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Comctl32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DPA_Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DPA_Clone function


## -description


<p class="CCE_Message">[<b>DPA_Clone</b> is available through Windows XP with Service Pack 2 (SP2). It might be altered or unavailable in subsequent versions.]

Duplicates a dynamic pointer array (DPA).


## -parameters




### -param hdpa [in]

Type: <b>const HDPA</b>

A handle to an existing DPA to copy.


### -param hdpaNew [in, out, optional]

Type: <b>HDPA</b>

When <b>NULL</b>, a new array is copied from <i>hdpaSource</i>. 

                    

This parameter can also contain an array created with <a href="https://msdn.microsoft.com/en-us/library/Bb775603(v=VS.85).aspx">DPA_Create</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb775605(v=VS.85).aspx">DPA_CreateEx</a>. The data is overwritten but the original delta size and heap handle retained.


## -returns



Type: <b>HDPA</b>

The handle to the new or altered DPA (<i>hdpaNew</i>) if successful; otherwise, <b>NULL</b>.




## -remarks



<b>DPA_Clone</b> is not exported by name or declared in a public header file. To use it, you must use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> and request ordinal 331 from ComCtl32.dll to obtain a function pointer.




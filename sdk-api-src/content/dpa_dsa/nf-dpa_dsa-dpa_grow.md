---
UID: NF:dpa_dsa.DPA_Grow
title: DPA_Grow function (dpa_dsa.h)
author: windows-sdk-content
description: Changes the number of pointers in a dynamic pointer array (DPA).
old-location: controls\DPA_Grow.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_grow.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DPA_Grow, DPA_Grow function [Windows Controls], _shell_DPA_Grow, _shell_DPA_Grow_cpp, controls.DPA_Grow, controls._shell_DPA_Grow, dpa_dsa/DPA_Grow
ms.topic: function
f1_keywords: 
 - "dpa_dsa/DPA_Grow"
dev_langs:
 - c++
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
 - DPA_Grow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DPA_Grow function


## -description


Changes the number of pointers in a dynamic pointer array (DPA).


## -parameters




### -param pdpa [in]

Type: <b>HDPA</b>

A handle to an existing DPA.


### -param cp [in]

Type: <b>int</b>

The number of pointers desired in the DPA.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



If <i>cp</i> is less than the number of pointers already in the DPA, the DPA is left unchanged. If <i>cp</i> is greater than the number of pointers in the DPA, the added pointers are initialized to <b>NULL</b>.




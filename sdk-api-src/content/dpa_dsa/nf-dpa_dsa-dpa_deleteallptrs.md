---
UID: NF:dpa_dsa.DPA_DeleteAllPtrs
title: DPA_DeleteAllPtrs function (dpa_dsa.h)
author: windows-sdk-content
description: Removes all items from a dynamic pointer array (DPA) and shrinks the DPA accordingly.
old-location: controls\DPA_DeleteAllPtrs.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_deleteallptrs.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DPA_DeleteAllPtrs, DPA_DeleteAllPtrs function [Windows Controls], _win32_DPA_DeleteAllPtrs, _win32_DPA_DeleteAllPtrs_cpp, controls.DPA_DeleteAllPtrs, controls._win32_DPA_DeleteAllPtrs, dpa_dsa/DPA_DeleteAllPtrs
ms.topic: function
f1_keywords: 
 - "dpa_dsa/DPA_DeleteAllPtrs"
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
req.lib: Comctl32.lib
req.dll: ComCtl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComCtl32.dll
api_name:
 - DPA_DeleteAllPtrs
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DPA_DeleteAllPtrs function


## -description


<p class="CCE_Message">[<b>DPA_DeleteAllPtrs</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Removes all items from a dynamic pointer array (DPA) and shrinks the DPA accordingly.


## -parameters




### -param hdpa

Type: <b>HDPA</b>

Handle to a DPA.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> on success or <b>FALSE</b> on failure.




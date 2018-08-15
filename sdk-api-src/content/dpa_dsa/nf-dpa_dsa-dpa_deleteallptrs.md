---
UID: NF:dpa_dsa.DPA_DeleteAllPtrs
title: DPA_DeleteAllPtrs function
author: windows-sdk-content
description: Removes all items from a dynamic pointer array (DPA) and shrinks the DPA accordingly.
old-location: controls\DPA_DeleteAllPtrs.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_deleteallptrs.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DPA_DeleteAllPtrs, DPA_DeleteAllPtrs function [Windows Controls], _win32_DPA_DeleteAllPtrs, _win32_DPA_DeleteAllPtrs_cpp, controls.DPA_DeleteAllPtrs, controls._win32_DPA_DeleteAllPtrs, dpa_dsa/DPA_DeleteAllPtrs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dpa_dsa.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CRYPTPROTECT_PROMPTSTRUCT, *PCRYPTPROTECT_PROMPTSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComCtl32.dll
api_name:
 - DPA_DeleteAllPtrs
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: ComCtl32.dll
req.irql: 
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



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> on success or <b>FALSE</b> on failure.




---
UID: NC:vdmdbg.TASKENUMPROCEX
title: TASKENUMPROCEX (vdmdbg.h)
description: Implement this function to receive information for each task that VDMEnumTaskWOWEx enumerates.
helpviewer_keywords: ["TASKENUMPROCEX","TASKENUMPROCEX callback","TASKENUMPROCEX callback function [Windows API]","vdmdbg/TASKENUMPROCEX","winprog.processtasks"]
old-location: winprog\processtasks.htm
tech.root: winprog
ms.assetid: 0ef6b3b0-1b65-4919-8857-33651b9c154f
ms.date: 12/05/2018
ms.keywords: TASKENUMPROCEX, TASKENUMPROCEX callback, TASKENUMPROCEX callback function [Windows API], vdmdbg/TASKENUMPROCEX, winprog.processtasks
req.header: vdmdbg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TASKENUMPROCEX
 - vdmdbg/TASKENUMPROCEX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - VdmDbg.h
api_name:
 - TASKENUMPROCEX
---

# TASKENUMPROCEX callback function


## -description

<p class="CCE_Message">[This function is not supported and may be altered or unavailable in the future.]

Implement this function to receive information for each task that <a href="/windows/desktop/api/vdmdbg/nf-vdmdbg-vdmenumtaskwowex">VDMEnumTaskWOWEx</a> enumerates. 
			

The <b>TASKENUMPROCEX</b> type defines a pointer to this callback function. <b>ProcessTasks</b> is a placeholder for the application-defined function name.

## -parameters

### -param dwThreadId [out]

The thread ID.

### -param hMod16 [out]

The module handle.

### -param hTask16 [out]

The task handle.

### -param pszModName [out]

The module name.

### -param pszFileName [out]

The file name.

### -param lpUserDefined [out]

The user-defined data that was passed to the <a href="/windows/desktop/api/vdmdbg/nf-vdmdbg-vdmenumtaskwowex">VDMEnumTaskWOWEx</a> function.

## -returns

Return <b>TRUE</b> to stop the enumeration and <b>FALSE</b> to continue.

## -remarks

You can use the value of the <i>hTask16</i> parameter in a call to terminate the task.
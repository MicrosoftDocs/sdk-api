---
UID: NF:shlobj_core.PifMgr_CloseProperties
title: PifMgr_CloseProperties function (shlobj_core.h)
description: Closes application properties that were opened with PifMgr_OpenProperties.
helpviewer_keywords: ["CLOSEPROPS_DISCARD","CLOSEPROPS_NONE","PifMgr_CloseProperties","PifMgr_CloseProperties function [Windows Properties]","_win32_PifMgr_CloseProperties","properties.PifMgr_CloseProperties","shell.PifMgr_CloseProperties","shlobj_core/PifMgr_CloseProperties"]
old-location: properties\PifMgr_CloseProperties.htm
tech.root: properties
ms.assetid: fd50d4f8-87c8-4162-9e88-3c8592b929fa
ms.date: 12/05/2018
ms.keywords: CLOSEPROPS_DISCARD, CLOSEPROPS_NONE, PifMgr_CloseProperties, PifMgr_CloseProperties function [Windows Properties], _win32_PifMgr_CloseProperties, properties.PifMgr_CloseProperties, shell.PifMgr_CloseProperties, shlobj_core/PifMgr_CloseProperties
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PifMgr_CloseProperties
 - shlobj_core/PifMgr_CloseProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - PifMgr_CloseProperties
---

# PifMgr_CloseProperties function


## -description

<p class="CCE_Message">[<b>PifMgr_CloseProperties</b> is available for use in the 

operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Closes application properties that were opened with <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pifmgr_openproperties">PifMgr_OpenProperties</a>.

## -parameters

### -param hProps [in]

Type: <b>HANDLE</b>

A handle to the application's properties. This parameter should be set to the value that is returned by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pifmgr_openproperties">PifMgr_OpenProperties</a>.

### -param flOpt [in]

Type: <b>UINT</b>

A flag that specifies how the function operates.



#### CLOSEPROPS_DISCARD

Abandon cached data.



#### CLOSEPROPS_NONE

No options specified.

## -returns

Type: <b>int</b>

Returns <b>NULL</b> if successful. If unsuccessful, the functions returns the handle to the application properties that was passed as <i>hProps</i>.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pifmgr_getproperties">PifMgr_GetProperties</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pifmgr_setproperties">PifMgr_SetProperties</a>
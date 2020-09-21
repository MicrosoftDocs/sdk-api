---
UID: NF:shlobj_core.IQueryInfo.GetInfoFlags
title: IQueryInfo::GetInfoFlags (shlobj_core.h)
description: Gets the information flags for an item. This method is not currently used.
helpviewer_keywords: ["GetInfoFlags","GetInfoFlags method [Windows Shell]","GetInfoFlags method [Windows Shell]","IQueryInfo interface","IQueryInfo interface [Windows Shell]","GetInfoFlags method","IQueryInfo.GetInfoFlags","IQueryInfo::GetInfoFlags","_win32_IQueryInfo_GetInfoFlags","shell.IQueryInfo_GetInfoFlags","shlobj_core/IQueryInfo::GetInfoFlags"]
old-location: shell\IQueryInfo_GetInfoFlags.htm
tech.root: shell
ms.assetid: 1baa47dd-b8e5-4535-b0eb-fd597241ed95
ms.date: 12/05/2018
ms.keywords: GetInfoFlags, GetInfoFlags method [Windows Shell], GetInfoFlags method [Windows Shell],IQueryInfo interface, IQueryInfo interface [Windows Shell],GetInfoFlags method, IQueryInfo.GetInfoFlags, IQueryInfo::GetInfoFlags, _win32_IQueryInfo_GetInfoFlags, shell.IQueryInfo_GetInfoFlags, shlobj_core/IQueryInfo::GetInfoFlags
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IQueryInfo::GetInfoFlags
 - shlobj_core/IQueryInfo::GetInfoFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IQueryInfo.GetInfoFlags
---

# IQueryInfo::GetInfoFlags


## -description

Gets the information flags for an item. This method is not currently used.

## -parameters

### -param pdwFlags [out]

Type: <b>DWORD*</b>

A pointer to a value that receives the flags for the item. If no flags are to be returned, this value should be set to zero.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if <i>pdwFlags</i> returns any flag values, or a COM-defined error value otherwise.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo">IQueryInfo</a>
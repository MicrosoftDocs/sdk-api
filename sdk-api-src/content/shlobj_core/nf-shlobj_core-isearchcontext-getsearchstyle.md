---
UID: NF:shlobj_core.ISearchContext.GetSearchStyle
title: ISearchContext::GetSearchStyle (shlobj_core.h)
description: Overrides the registry settings that determine how an autosearch is performed.
helpviewer_keywords: ["GetSearchStyle","GetSearchStyle method [Windows Shell]","GetSearchStyle method [Windows Shell]","ISearchContext interface","ISearchContext interface [Windows Shell]","GetSearchStyle method","ISearchContext.GetSearchStyle","ISearchContext::GetSearchStyle","_shell_ISearchContext_GetSearchStyle","shell.ISearchContext_GetSearchStyle","shlobj_core/ISearchContext::GetSearchStyle"]
old-location: shell\ISearchContext_GetSearchStyle.htm
tech.root: shell
ms.assetid: d2ea6201-fd70-46de-8270-c0cc34c728aa
ms.date: 12/05/2018
ms.keywords: GetSearchStyle, GetSearchStyle method [Windows Shell], GetSearchStyle method [Windows Shell],ISearchContext interface, ISearchContext interface [Windows Shell],GetSearchStyle method, ISearchContext.GetSearchStyle, ISearchContext::GetSearchStyle, _shell_ISearchContext_GetSearchStyle, shell.ISearchContext_GetSearchStyle, shlobj_core/ISearchContext::GetSearchStyle
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISearchContext::GetSearchStyle
 - shlobj_core/ISearchContext::GetSearchStyle
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
 - ISearchContext.GetSearchStyle
---

# ISearchContext::GetSearchStyle


## -description

Overrides the registry settings that determine how an autosearch is performed.

## -parameters

### -param pdwSearchStyle [in]

Type: <b>DWORD</b>

A pointer to a <b>DWORD</b> value that indicates how the search is performed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.


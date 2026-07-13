---
UID: NF:shobjidl.ICommDlgBrowser3.GetCurrentFilter
title: ICommDlgBrowser3::GetCurrentFilter (shobjidl.h)
description: Gets the current filter as a Unicode string.
helpviewer_keywords: ["GetCurrentFilter","GetCurrentFilter method [Windows Shell]","GetCurrentFilter method [Windows Shell]","ICommDlgBrowser3 interface","ICommDlgBrowser3 interface [Windows Shell]","GetCurrentFilter method","ICommDlgBrowser3.GetCurrentFilter","ICommDlgBrowser3::GetCurrentFilter","_shell_ICommDlgBrowser3_GetCurrentFilter","shell.ICommDlgBrowser3_GetCurrentFilter","shobjidl/ICommDlgBrowser3::GetCurrentFilter"]
old-location: shell\ICommDlgBrowser3_GetCurrentFilter.htm
tech.root: shell
ms.assetid: 038f3478-82d0-4023-a787-b7a2c66ceb27
ms.date: 12/05/2018
ms.keywords: GetCurrentFilter, GetCurrentFilter method [Windows Shell], GetCurrentFilter method [Windows Shell],ICommDlgBrowser3 interface, ICommDlgBrowser3 interface [Windows Shell],GetCurrentFilter method, ICommDlgBrowser3.GetCurrentFilter, ICommDlgBrowser3::GetCurrentFilter, _shell_ICommDlgBrowser3_GetCurrentFilter, shell.ICommDlgBrowser3_GetCurrentFilter, shobjidl/ICommDlgBrowser3::GetCurrentFilter
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - ICommDlgBrowser3::GetCurrentFilter
 - shobjidl/ICommDlgBrowser3::GetCurrentFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - ICommDlgBrowser3.GetCurrentFilter
---

# ICommDlgBrowser3::GetCurrentFilter


## -description

Gets the current filter as a Unicode string.

## -parameters

### -param pszFileSpec [out]

Type: <b>LPWSTR</b>

Contains a pointer to the current filter path/file as a Unicode string.

### -param cchFileSpec [in]

Type: <b>int</b>

Specifies the path/file length, in characters.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.


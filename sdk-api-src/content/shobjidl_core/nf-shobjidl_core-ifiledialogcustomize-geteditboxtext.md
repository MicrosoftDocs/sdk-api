---
UID: NF:shobjidl_core.IFileDialogCustomize.GetEditBoxText
title: IFileDialogCustomize::GetEditBoxText (shobjidl_core.h)
description: Gets the current text in an edit box control.
helpviewer_keywords: ["GetEditBoxText","GetEditBoxText method [Windows Shell]","GetEditBoxText method [Windows Shell]","IFileDialogCustomize interface","IFileDialogCustomize interface [Windows Shell]","GetEditBoxText method","IFileDialogCustomize.GetEditBoxText","IFileDialogCustomize::GetEditBoxText","shell.IFileDialogCustomize_GetEditBoxText","shell_IFileDialogCustomize_GetEditBoxText","shobjidl_core/IFileDialogCustomize::GetEditBoxText"]
old-location: shell\IFileDialogCustomize_GetEditBoxText.htm
tech.root: shell
ms.assetid: 7c3db511-d357-48b4-9ac3-07f6b3d23a5f
ms.date: 12/05/2018
ms.keywords: GetEditBoxText, GetEditBoxText method [Windows Shell], GetEditBoxText method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],GetEditBoxText method, IFileDialogCustomize.GetEditBoxText, IFileDialogCustomize::GetEditBoxText, shell.IFileDialogCustomize_GetEditBoxText, shell_IFileDialogCustomize_GetEditBoxText, shobjidl_core/IFileDialogCustomize::GetEditBoxText
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - IFileDialogCustomize::GetEditBoxText
 - shobjidl_core/IFileDialogCustomize::GetEditBoxText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileDialogCustomize.GetEditBoxText
---

# IFileDialogCustomize::GetEditBoxText


## -description

Gets the current text in an edit box control.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the edit box.

### -param ppszText [out]

Type: <b>WCHAR**</b>

The address of a pointer to a buffer that receives the text as a null-terminated Unicode string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

It is the responsibility of the calling application to free the buffer referenced by <i>ppszText</i> when it is no longer needed. Use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to free the buffer.
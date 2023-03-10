---
UID: NF:shobjidl.ISearchBoxInfo.GetText
title: ISearchBoxInfo::GetText (shobjidl.h)
description: Retrieves the contents of the search box as plain text.
helpviewer_keywords: ["GetText","GetText method [Windows Shell]","GetText method [Windows Shell]","ISearchBoxInfo interface","ISearchBoxInfo interface [Windows Shell]","GetText method","ISearchBoxInfo.GetText","ISearchBoxInfo::GetText","_shell_ISearchBoxInfo_GetText","shell.ISearchBoxInfo_GetText","shobjidl/ISearchBoxInfo::GetText"]
old-location: shell\ISearchBoxInfo_GetText.htm
tech.root: shell
ms.assetid: 2bfb65d5-a27e-41f7-883e-2e1afe912586
ms.date: 12/05/2018
ms.keywords: GetText, GetText method [Windows Shell], GetText method [Windows Shell],ISearchBoxInfo interface, ISearchBoxInfo interface [Windows Shell],GetText method, ISearchBoxInfo.GetText, ISearchBoxInfo::GetText, _shell_ISearchBoxInfo_GetText, shell.ISearchBoxInfo_GetText, shobjidl/ISearchBoxInfo::GetText
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - ISearchBoxInfo::GetText
 - shobjidl/ISearchBoxInfo::GetText
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
 - ISearchBoxInfo.GetText
---

# ISearchBoxInfo::GetText


## -description

Retrieves the contents of the search box as plain text.

## -parameters

### -param ppsz [out]

Type: <b>LPWSTR*</b>

Pointer to a buffer that, when this method returns successfully, receives the full text entered in the search box.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-isearchboxinfo">ISearchBoxInfo</a>
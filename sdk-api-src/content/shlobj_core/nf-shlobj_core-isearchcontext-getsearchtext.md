---
UID: NF:shlobj_core.ISearchContext.GetSearchText
title: ISearchContext::GetSearchText (shlobj_core.h)
description: Retrieves the text that is in the browser's Address bar.
helpviewer_keywords: ["GetSearchText","GetSearchText method [Windows Shell]","GetSearchText method [Windows Shell]","ISearchContext interface","ISearchContext interface [Windows Shell]","GetSearchText method","ISearchContext.GetSearchText","ISearchContext::GetSearchText","_shell_ISearchContext_GetSearchText","shell.ISearchContext_GetSearchText","shlobj_core/ISearchContext::GetSearchText"]
old-location: shell\ISearchContext_GetSearchText.htm
tech.root: shell
ms.assetid: d38946be-8fd3-46e2-953e-8e94bcad4b81
ms.date: 12/05/2018
ms.keywords: GetSearchText, GetSearchText method [Windows Shell], GetSearchText method [Windows Shell],ISearchContext interface, ISearchContext interface [Windows Shell],GetSearchText method, ISearchContext.GetSearchText, ISearchContext::GetSearchText, _shell_ISearchContext_GetSearchText, shell.ISearchContext_GetSearchText, shlobj_core/ISearchContext::GetSearchText
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
 - ISearchContext::GetSearchText
 - shlobj_core/ISearchContext::GetSearchText
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
 - ISearchContext.GetSearchText
---

# ISearchContext::GetSearchText


## -description

Retrieves the text that is in the browser's Address bar.

## -parameters

### -param pbstrSearchText [in]

Type: <b><a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a></b>

The <b>BSTR</b> that receives the text in the Address bar.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
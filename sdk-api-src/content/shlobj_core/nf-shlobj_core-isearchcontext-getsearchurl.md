---
UID: NF:shlobj_core.ISearchContext.GetSearchUrl
title: ISearchContext::GetSearchUrl (shlobj_core.h)
description: Retrieves the URL that is being searched for.
helpviewer_keywords: ["GetSearchURL method [Windows Shell]","GetSearchURL method [Windows Shell]","ISearchContext interface","GetSearchUrl","ISearchContext interface [Windows Shell]","GetSearchURL method","ISearchContext.GetSearchUrl","ISearchContext::GetSearchURL","ISearchContext::GetSearchUrl","_shell_ISearchContext_GetSearchURL","shell.ISearchContext_GetSearchURL","shlobj_core/ISearchContext::GetSearchURL"]
old-location: shell\ISearchContext_GetSearchURL.htm
tech.root: shell
ms.assetid: b2c9034f-65a2-414c-b440-330413ae63ce
ms.date: 12/05/2018
ms.keywords: GetSearchURL method [Windows Shell], GetSearchURL method [Windows Shell],ISearchContext interface, GetSearchUrl, ISearchContext interface [Windows Shell],GetSearchURL method, ISearchContext.GetSearchUrl, ISearchContext::GetSearchURL, ISearchContext::GetSearchUrl, _shell_ISearchContext_GetSearchURL, shell.ISearchContext_GetSearchURL, shlobj_core/ISearchContext::GetSearchURL
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shlobj.idl
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
 - ISearchContext::GetSearchUrl
 - shlobj_core/ISearchContext::GetSearchUrl
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
 - ISearchContext.GetSearchURL
---

# ISearchContext::GetSearchUrl


## -description

Retrieves the URL that is being searched for.

## -parameters

### -param pbstrSearchUrl [in]

Type: <b><a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a></b>

The <b>BSTR</b> that receives the URL.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
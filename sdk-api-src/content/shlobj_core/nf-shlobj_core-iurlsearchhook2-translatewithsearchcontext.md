---
UID: NF:shlobj_core.IURLSearchHook2.TranslateWithSearchContext
title: IURLSearchHook2::TranslateWithSearchContext
author: windows-sdk-content
description: Called by the browser when the browser cannot determine the protocol of a URL address. This method uses a search context to determine the protocol.
old-location: shell\IURLSearchHook2_TranslateWithSearchContext.htm
old-project: shell
ms.assetid: 6143a642-e003-4268-b146-0d3d5cc907df
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IURLSearchHook2 interface [Windows Shell],TranslateWithSearchContext method, IURLSearchHook2.TranslateWithSearchContext, IURLSearchHook2::TranslateWithSearchContext, TranslateWithSearchContext, TranslateWithSearchContext method [Windows Shell], TranslateWithSearchContext method [Windows Shell],IURLSearchHook2 interface, _shell_IURLSearchHook2_TranslateWithSearchContext, shell.IURLSearchHook2_TranslateWithSearchContext, shlobj_core/IURLSearchHook2::TranslateWithSearchContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IURLSearchHook2.TranslateWithSearchContext
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# IURLSearchHook2::TranslateWithSearchContext


## -description


Called by the browser when the browser cannot determine the protocol of a URL address. This method uses a search context to determine the protocol.


## -parameters




### -param pwszSearchURL [out]

Type: <b>PWSTR</b>

The address of a wide character buffer that, on entry, contains the URL address for which the browser is trying to determine the protocol. On exit, this buffer contains the modified URL address if the method was successful.


### -param cchBufferSize

Type: <b>DWORD</b>

The size, in characters, of the buffer at <i>lpwszSearchURL</i>.


### -param pSearchContext [in, optional]

Type: <b><a href="https://msdn.microsoft.com/95ac188a-f27f-4e09-9de3-a822bbbd6e8e">ISearchContext</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/95ac188a-f27f-4e09-9de3-a822bbbd6e8e">ISearchContext</a> object. This parameter can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




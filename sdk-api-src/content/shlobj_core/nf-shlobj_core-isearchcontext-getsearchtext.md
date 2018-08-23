---
UID: NF:shlobj_core.ISearchContext.GetSearchText
title: ISearchContext::GetSearchText
author: windows-sdk-content
description: Retrieves the text that is in the browser's Address bar.
old-location: shell\ISearchContext_GetSearchText.htm
old-project: shell
ms.assetid: d38946be-8fd3-46e2-953e-8e94bcad4b81
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetSearchText, GetSearchText method [Windows Shell], GetSearchText method [Windows Shell],ISearchContext interface, ISearchContext interface [Windows Shell],GetSearchText method, ISearchContext.GetSearchText, ISearchContext::GetSearchText, _shell_ISearchContext_GetSearchText, shell.ISearchContext_GetSearchText, shlobj_core/ISearchContext::GetSearchText
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
 - ISearchContext.GetSearchText
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# ISearchContext::GetSearchText


## -description


Retrieves the text that is in the browser's Address bar.


## -parameters




### -param pbstrSearchText [in]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>

The <b>BSTR</b> that receives the text in the Address bar.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




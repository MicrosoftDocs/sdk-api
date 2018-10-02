---
UID: NF:shlobj_core.ISearchContext.GetSearchUrl
title: ISearchContext::GetSearchUrl
author: windows-sdk-content
description: Retrieves the URL that is being searched for.
old-location: shell\ISearchContext_GetSearchURL.htm
tech.root: Shell
ms.assetid: b2c9034f-65a2-414c-b440-330413ae63ce
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetSearchURL method [Windows Shell], GetSearchURL method [Windows Shell],ISearchContext interface, GetSearchUrl, ISearchContext interface [Windows Shell],GetSearchURL method, ISearchContext.GetSearchUrl, ISearchContext::GetSearchURL, ISearchContext::GetSearchUrl, _shell_ISearchContext_GetSearchURL, shell.ISearchContext_GetSearchURL, shlobj_core/ISearchContext::GetSearchURL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ISearchContext.GetSearchURL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISearchContext::GetSearchUrl


## -description


Retrieves the URL that is being searched for.


## -parameters




### -param pbstrSearchUrl

TBD




#### - pbstrSearchURL [in]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>

The <b>BSTR</b> that receives the URL.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




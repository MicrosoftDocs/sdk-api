---
UID: NF:searchapi.IUrlAccessor.GetRedirectedURL
title: IUrlAccessor::GetRedirectedURL
author: windows-sdk-content
description: Gets the redirected URL for the current item.
old-location: search\_search_IUrlAccessor_GetRedirectedURL.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\getredirectedurl.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetRedirectedURL, GetRedirectedURL method [search], GetRedirectedURL method [search],IUrlAccessor interface, IUrlAccessor interface [search],GetRedirectedURL method, IUrlAccessor.GetRedirectedURL, IUrlAccessor::GetRedirectedURL, _search_IUrlAccessor_GetRedirectedURL, search._search_IUrlAccessor_GetRedirectedURL, searchapi/IUrlAccessor::GetRedirectedURL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Urlaccsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - IUrlAccessor.GetRedirectedURL
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IUrlAccessor::GetRedirectedURL


## -description


Gets the redirected URL for the current item.
        


## -parameters




### -param wszRedirectedURL [out]

Type: <b>WCHAR[]</b>

Receives the redirected URL as a Unicode string, not including the terminating <b>NULL</b>.
                


### -param dwSize [in]

Type: <b>DWORD</b>

Size in <b>TCHAR</b><b>s</b>of <i>wszRedirectedURL</i>, not including the terminating <b>NULL</b>.
                


### -param pdwLength [out]

Type: <b>DWORD*</b>

Receives a pointer to the number of
                <b>TCHAR</b><b>s</b> 
                written to <i>wszRedirectedURL</i>,
                not including the terminating <b>NULL</b>.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



File URLs are not redirected. This method applies only to a content source of HTTP.
            

If this method is implemented, the URL that is passed to <a href="https://msdn.microsoft.com/6fa8bf02-155d-48e9-8f94-c54680ae33e2">ISearchProtocol::CreateAccessor</a> will be redirected to the value returned by this method. All subsequent relative URL links will be processed based on the redirected URL.
            




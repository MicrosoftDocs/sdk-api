---
UID: NF:searchapi.IUrlAccessor.GetHost
title: IUrlAccessor::GetHost
author: windows-sdk-content
description: Gets the host name for the content source, if applicable.
old-location: search\_search_IUrlAccessor_GetHost.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\gethost.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetHost, GetHost method [search], GetHost method [search],IUrlAccessor interface, IUrlAccessor interface [search],GetHost method, IUrlAccessor.GetHost, IUrlAccessor::GetHost, _search_IUrlAccessor_GetHost, search._search_IUrlAccessor_GetHost, searchapi/IUrlAccessor::GetHost
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
 - IUrlAccessor.GetHost
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- COM
: 
- searchapi.h
: 
- IUrlAccessor.GetHost
: 
---

# IUrlAccessor::GetHost


## -description


Gets the host name for the content source, if applicable.
        


## -parameters




### -param wszHost [out]

Type: <b>WCHAR[]</b>

Receives the name of the host that the content source file resides on, as a null-terminated Unicode string.
                


### -param dwSize [in]

Type: <b>DWORD</b>

Size in <b>TCHAR</b><b>s</b>of <i>wszHost</i>, not including the terminating <b>NULL</b>.
                


### -param pdwLength [out]

Type: <b>DWORD*</b>

Receives a pointer to the number of <b>TCHAR</b><b>s</b> written to <i>wszHost</i>, not including the terminating <b>NULL</b>. 
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




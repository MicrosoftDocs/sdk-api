---
UID: NF:searchapi.IUrlAccessor2.GetDisplayUrl
title: IUrlAccessor2::GetDisplayUrl
author: windows-sdk-content
description: Gets the user-friendly path for the URL item.
old-location: search\_search_IUrlAccessor2_GetDisplayUrl.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor2\getdisplayurl.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetDisplayUrl, GetDisplayUrl method [search], GetDisplayUrl method [search],IUrlAccessor2 interface, GetDisplayUrl method [search],IUrlAccessor4 interface, IUrlAccessor2 interface [search],GetDisplayUrl method, IUrlAccessor2.GetDisplayUrl, IUrlAccessor2::GetDisplayUrl, IUrlAccessor4 interface [search],GetDisplayUrl method, IUrlAccessor4::GetDisplayUrl, _search_IUrlAccessor2_GetDisplayUrl, search._search_IUrlAccessor2_GetDisplayUrl, searchapi/IUrlAccessor2::GetDisplayUrl, searchapi/IUrlAccessor4::GetDisplayUrl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IUrlAccessor2.GetDisplayUrl
 - IUrlAccessor4.GetDisplayUrl
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IUrlAccessor2::GetDisplayUrl


## -description


Gets the user-friendly path for the URL item.
        


## -parameters




### -param wszDocUrl [out]

Type: <b>WCHAR[]</b>

Receives the display URL as a null-terminated Unicode string.
                


### -param dwSize [in]

Type: <b>DWORD</b>

Size in <b>TCHAR</b><b>s</b>of <i>wszDocUrl</i>.
                


### -param pdwLength [out]

Type: <b>DWORD*</b>

Receives a pointer to the number of
                <b>TCHAR</b><b>s</b> written
                to <i>wszDocUrl</i>, not including the terminating <b>NULL</b>. 
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Protocol handlers can reveal hierarchical or non-hierarchical stores. If the data store is organized hierarchically, users can scope their searches to a specified container object like a directory or folder. 





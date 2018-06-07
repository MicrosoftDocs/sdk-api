---
UID: NF:searchapi.IUrlAccessor.GetLastModified
title: IUrlAccessor::GetLastModified
author: windows-sdk-content
description: Gets the time stamp identifying when the URL was last modified.
old-location: search\_search_IUrlAccessor_GetLastModified.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\getlastmodified.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetLastModified, GetLastModified method [search], GetLastModified method [search],IUrlAccessor interface, IUrlAccessor interface [search],GetLastModified method, IUrlAccessor.GetLastModified, IUrlAccessor::GetLastModified, _search_IUrlAccessor_GetLastModified, search._search_IUrlAccessor_GetLastModified, searchapi/IUrlAccessor::GetLastModified
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - IUrlAccessor.GetLastModified
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IUrlAccessor::GetLastModified


## -description



        Gets the time stamp identifying when the URL was last modified.
        


## -parameters




### -param pftLastModified [out]

Type: <b><a href="https://www.bing.com/search?q=FILETIME">FILETIME</a>*</b>


                Receives a pointer to a variable of type <a href="https://www.bing.com/search?q=FILETIME">FILETIME</a> identifying the time stamp when the URL was last modified.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is used to determine whether a URL has changed since the last time it was indexed. If the last modified time has not changed, the indexer does not process the URL's content.  
            

Directory URLs are always processed regardless of the time stamp returned by this method.
            




---
UID: NF:searchapi.IUrlAccessor.BindToFilter
title: IUrlAccessor::BindToFilter
author: windows-sdk-content
description: Binds the item being processed to the appropriate IFilterand retrieves a pointer to the IFilter.
old-location: search\_search_IUrlAccessor_BindToFilter.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\bindtofilter.htm
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: BindToFilter, BindToFilter method [search], BindToFilter method [search],IUrlAccessor interface, IUrlAccessor interface [search],BindToFilter method, IUrlAccessor.BindToFilter, IUrlAccessor::BindToFilter, _search_IUrlAccessor_BindToFilter, search._search_IUrlAccessor_BindToFilter, searchapi/IUrlAccessor::BindToFilter
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
 - IUrlAccessor.BindToFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IUrlAccessor::BindToFilter


## -description


Binds the item being processed to the appropriate <a href="https://msdn.microsoft.com/en-us/library/ms691105(v=VS.85).aspx">IFilter</a>and retrieves a pointer to the <b>IFilter</b>.
        


## -parameters




### -param ppFilter [out]

Type: <b>IFilter**</b>

Receives the address of a pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms691105(v=VS.85).aspx">IFilter</a> that can return metadata about the item being processed.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method retrieves an <a href="https://msdn.microsoft.com/en-us/library/ms691105(v=VS.85).aspx">IFilter</a> to enumerate the properties of the item associated with the specified URL, based on the protocol's information about that URL.
            

If the URL's content is also accessible from the <a href="https://msdn.microsoft.com/en-us/library/Aa380034(v=VS.85).aspx">IStream</a> returned by <a href="https://msdn.microsoft.com/en-us/library/Bb231415(v=VS.85).aspx">IUrlAccessor::BindToStream</a>, then a separate <a href="https://msdn.microsoft.com/en-us/library/ms691105(v=VS.85).aspx">IFilter</a>is invoked on the IStream to retrieve additional properties.
            




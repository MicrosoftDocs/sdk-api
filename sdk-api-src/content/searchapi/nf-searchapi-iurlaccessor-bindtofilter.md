---
UID: NF:searchapi.IUrlAccessor.BindToFilter
title: IUrlAccessor::BindToFilter
author: windows-sdk-content
description: Binds the item being processed to the appropriate IFilterand retrieves a pointer to the IFilter.
old-location: search\_search_IUrlAccessor_BindToFilter.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\bindtofilter.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: BindToFilter, BindToFilter method [search], BindToFilter method [search],IUrlAccessor interface, IUrlAccessor interface [search],BindToFilter method, IUrlAccessor.BindToFilter, IUrlAccessor::BindToFilter, _search_IUrlAccessor_BindToFilter, search._search_IUrlAccessor_BindToFilter, searchapi/IUrlAccessor::BindToFilter
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	IUrlAccessor.BindToFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IUrlAccessor::BindToFilter


## -description



        Binds the item being processed to the appropriate <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>and retrieves a pointer to the <b>IFilter</b>.
        


## -parameters




### -param ppFilter [out]

Type: <b>IFilter**</b>

Receives the address of a pointer to the <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> that can return metadata about the item being processed.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method retrieves an <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a> to enumerate the properties of the item associated with the specified URL, based on the protocol's information about that URL.
            

If the URL's content is also accessible from the <a href="_stg_istream">IStream</a> returned by <a href="https://msdn.microsoft.com/02dc13c0-01a4-416d-ba14-c0390b4c4aae">IUrlAccessor::BindToStream</a>, then a separate <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>is invoked on the IStream to retrieve additional properties.
            




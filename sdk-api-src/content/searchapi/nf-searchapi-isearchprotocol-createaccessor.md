---
UID: NF:searchapi.ISearchProtocol.CreateAccessor
title: ISearchProtocol::CreateAccessor (searchapi.h)
author: windows-sdk-content
description: Creates and initializes an IUrlAccessor object.
old-location: search\_search_ISearchProtocol_CreateAccessor.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocol\createaccessor.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateAccessor, CreateAccessor method [search], CreateAccessor method [search],ISearchProtocol interface, ISearchProtocol interface [search],CreateAccessor method, ISearchProtocol.CreateAccessor, ISearchProtocol::CreateAccessor, _search_ISearchProtocol_CreateAccessor, search._search_ISearchProtocol_CreateAccessor, searchapi/ISearchProtocol::CreateAccessor
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
req.idl: Srchprth.idl
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
 - ISearchProtocol.CreateAccessor
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchProtocol::CreateAccessor


## -description


Creates and initializes an <a href="https://msdn.microsoft.com/en-us/library/Bb231426(v=VS.85).aspx">IUrlAccessor</a> object.  
        


## -parameters




### -param pcwszURL [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string containing the URL of the item being accessed. 
                


### -param pAuthenticationInfo [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa965364(v=VS.85).aspx">AUTHENTICATION_INFO</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa965364(v=VS.85).aspx">AUTHENTICATION_INFO</a> structure that contains authentication information necessary for accessing this item in the content source. 
                


### -param pIncrementalAccessInfo [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa965366(v=VS.85).aspx">INCREMENTAL_ACCESS_INFO</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa965366(v=VS.85).aspx">INCREMENTAL_ACCESS_INFO</a> structure that contains incremental access information, such as the last time the file was accessed by the gatherer. 
                


### -param pItemInfo [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa965368(v=VS.85).aspx">ITEM_INFO</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa965368(v=VS.85).aspx">ITEM_INFO</a> structure that contains information about the URL item, such as the name of the item's workspace catalog.
                


### -param ppAccessor [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb231426(v=VS.85).aspx">IUrlAccessor</a>**</b>

Receives the address of a pointer to the  <a href="https://msdn.microsoft.com/en-us/library/Bb231426(v=VS.85).aspx">IUrlAccessor</a> object created by this method. This object contains information about the URL item, such as the item's file name.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 
       The protocol host calls this method on the protocol handler once for every URL processed by the gatherer and retrieves a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb231426(v=VS.85).aspx">IUrlAccessor</a> object. This method creates and initializes an <b>IUrlAccessor</b> object to process an item currently being accessed by the gatherer.
      




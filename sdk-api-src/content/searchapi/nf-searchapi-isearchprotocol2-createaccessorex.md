---
UID: NF:searchapi.ISearchProtocol2.CreateAccessorEx
title: ISearchProtocol2::CreateAccessorEx
author: windows-sdk-content
description: Creates and initializes an IUrlAccessor object. This method has the same basic functionality as the ISearchProtocol::CreateAccessor method, but it includes an additional pUserData parameter to supply additional data to the protocol handler.
old-location: search\_search_ISearchProtocol2_CreateAccessorEx.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\isearchprotocol2\createaccessorex.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: CreateAccessorEx, CreateAccessorEx method [search], CreateAccessorEx method [search],ISearchProtocol2 interface, ISearchProtocol2 interface [search],CreateAccessorEx method, ISearchProtocol2.CreateAccessorEx, ISearchProtocol2::CreateAccessorEx, _search_ISearchProtocol2_CreateAccessorEx, search._search_ISearchProtocol2_CreateAccessorEx, searchapi/ISearchProtocol2::CreateAccessorEx
ms.prod: windows
ms.technology: windows-sdk
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
req.idl: Srchprth.idl
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
 - ISearchProtocol2.CreateAccessorEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISearchProtocol2::CreateAccessorEx


## -description


 
        Creates and initializes an <a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a> object. This method has the same basic functionality as the <a href="https://msdn.microsoft.com/6fa8bf02-155d-48e9-8f94-c54680ae33e2">ISearchProtocol::CreateAccessor</a> method, but it includes an additional <b>pUserData</b> parameter to supply additional data to the protocol handler.
        


## -parameters




### -param pcwszURL [in]

Type: <b>LPCWSTR</b>


                Pointer to a null-terminated Unicode string containing the URL of the item being accessed.
                


### -param pAuthenticationInfo [in]

Type: <b><a href="https://msdn.microsoft.com/e982fcb2-9fc6-4f7b-bdb5-1e480fd98b0b">AUTHENTICATION_INFO</a>*</b>


                Pointer to an <a href="https://msdn.microsoft.com/e982fcb2-9fc6-4f7b-bdb5-1e480fd98b0b">AUTHENTICATION_INFO</a> structure that contains authentication information necessary for accessing this item in the content source. 
                


### -param pIncrementalAccessInfo [in]

Type: <b><a href="https://msdn.microsoft.com/f6fb7519-e473-4ab9-b65b-18d4ac7ea158">INCREMENTAL_ACCESS_INFO</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/f6fb7519-e473-4ab9-b65b-18d4ac7ea158">INCREMENTAL_ACCESS_INFO</a> structure that contains incremental access information, such as the last time the file was accessed by the gatherer. 



### -param pItemInfo [in]

Type: <b><a href="https://msdn.microsoft.com/08acc675-db1c-4856-a67b-25b4d83f4350">ITEM_INFO</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/08acc675-db1c-4856-a67b-25b4d83f4350">ITEM_INFO</a> structure that contains information about the URL item, such as the name of the item's workspace catalog.


### -param pUserData [in]

Type: <b>const BLOB*</b>


          Pointer to user information. This data can be whatever the notification originator decides. If the protocol handler implements this interface, it will receive this data.  Not all notifications have this blob set.
        


### -param ppAccessor [out]

Type: <b><a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a>**</b>


                Receives the address of a pointer to the <a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a> object created by this method. This object contains information about the URL item, such as the item's file name.
               


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




         This method creates and initializes an <a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a> object to process an item currently being accessed by the gatherer. The protocol host calls this method on the protocol handler. This method is called once for every URL processed by the gatherer and retrieves a pointer to the <b>IUrlAccessor</b> object. 





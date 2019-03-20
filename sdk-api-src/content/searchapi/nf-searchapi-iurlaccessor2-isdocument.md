---
UID: NF:searchapi.IUrlAccessor2.IsDocument
title: IUrlAccessor2::IsDocument (searchapi.h)
author: windows-sdk-content
description: Ascertains whether an item URL is a document or directory.
old-location: search\_search_IUrlAccessor2_IsDocument.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor2\isdocument.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUrlAccessor2 interface [search],IsDocument method, IUrlAccessor2.IsDocument, IUrlAccessor2::IsDocument, IUrlAccessor4 interface [search],IsDocument method, IUrlAccessor4::IsDocument, IsDocument, IsDocument method [search], IsDocument method [search],IUrlAccessor2 interface, IsDocument method [search],IUrlAccessor4 interface, _search_IUrlAccessor2_IsDocument, search._search_IUrlAccessor2_IsDocument, searchapi/IUrlAccessor2::IsDocument, searchapi/IUrlAccessor4::IsDocument
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
 - IUrlAccessor2.IsDocument
 - IUrlAccessor4.IsDocument
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IUrlAccessor2::IsDocument


## -description


Ascertains whether an item URL is a document or directory.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_FALSE if the item is a directory; otherwise, it returns S_OK.




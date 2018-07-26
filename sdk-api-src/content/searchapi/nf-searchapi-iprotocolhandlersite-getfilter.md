---
UID: NF:searchapi.IProtocolHandlerSite.GetFilter
title: IProtocolHandlerSite::GetFilter
author: windows-sdk-content
description: Retrieves the appropriate IFilteraccording to the supplied parameters.
old-location: search\_search_IProtocolHandlerSite_search_IProtocolHandlerSite_GetFilter_cpp.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iprotocolhandlersite\getfilter.htm
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: GetFilter, GetFilter method [search], GetFilter method [search],IProtocolHandlerSite interface, IProtocolHandlerSite interface [search],GetFilter method, IProtocolHandlerSite.GetFilter, IProtocolHandlerSite::GetFilter, _search_IProtocolHandlerSite_GetFilter, search._search_IProtocolHandlerSite_GetFilter, search._search_IProtocolHandlerSite_search_IProtocolHandlerSite_GetFilter_cpp, searchapi/IProtocolHandlerSite::GetFilter
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
 - IProtocolHandlerSite.GetFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IProtocolHandlerSite::GetFilter


## -description



        Retrieves the appropriate <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>according to the supplied parameters.     
        


## -parameters




### -param pclsidObj [in]

Type: <b>CLSID*</b>

Pointer to the CLSID of the document type from the registry. This is used for items with embedded documents to indicate the appropriate <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>to use for that embedded document.


### -param pcwszContentType [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string that contains the type of the document. This is used to retrieve <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a><b>s</b> that are mapped according to MIME type.


### -param pcwszExtension [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string that contains the file name extension, without the preceding period. This is used to retrieve <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>objects that are mapped according to the file name extension.


### -param ppFilter [out]

Type: <b>IFilter**</b>

Receives the address of a pointer to the <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>that the protocol handler uses.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method queries the Filter Host to identify the appropriate <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>object to use for the URL item.

The choice of filter is based on the file name extension, a CLSID that identifies the file's content type in the registry, or on the MIME content type. You need to provide only one of the three parameters to this method. If you provide multiple parameters, they are tested in the following order: <i>pcwszContentType</i>, <i>pclsidObj</i>, <i>pcwszExtension</i>. The first valid parameter is used to select the appropriate <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>; the others are ignored.




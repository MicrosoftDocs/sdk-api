---
UID: NN:searchapi.IUrlAccessor
title: IUrlAccessor (searchapi.h)
description: Provides methods for processing an individual item in a content source whose URL is provided by the gatherer to the filter host.helpviewer_keywords: ["IUrlAccessor","IUrlAccessor interface [search]","IUrlAccessor interface [search]","described","_search_IUrlAccessor","search._search_IUrlAccessor","searchapi/IUrlAccessor"]
old-location: search\_search_IUrlAccessor.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\iurlaccessor.htm
ms.date: 12/05/2018
ms.keywords: IUrlAccessor, IUrlAccessor interface [search], IUrlAccessor interface [search],described, _search_IUrlAccessor, search._search_IUrlAccessor, searchapi/IUrlAccessor
f1_keywords:
- searchapi/IUrlAccessor
dev_langs:
- c++
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
- IUrlAccessor
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# IUrlAccessor interface


## -description


Provides methods for processing an individual item in a content source whose URL is provided by the gatherer to the filter host.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUrlAccessor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUrlAccessor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUrlAccessor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-addrequestparameter">AddRequestParameter</a>
</td>
<td align="left" width="63%">
Requests a property-value set. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-bindtofilter">BindToFilter</a>
</td>
<td align="left" width="63%">
Binds the item being processed to the appropriate <a href="https://docs.microsoft.com/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a>and retrieves a pointer to the <b>IFilter</b>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-bindtostream">BindToStream</a>
</td>
<td align="left" width="63%">
Binds the item being processed to an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream interface [Structured Storage]</a> data stream and retrieves a pointer to that stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-getclsid">GetCLSID</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/com/clsid">CLSID</a> for the document type of the URL item being processed.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-getdocformat">GetDocFormat</a>
</td>
<td align="left" width="63%">
Gets the document format, represented as a Multipurpose Internet Mail Extensions (MIME) string.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-getfilename">GetFileName</a>
</td>
<td align="left" width="63%">
Retrieves the file name of the item, which the filter host uses for indexing. If the item does not exist in a file system and the <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-bindtostream">IUrlAccessor::BindToStream</a> method is implemented, this method returns the shell's System.ParsingPath property for the item. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-gethost">GetHost</a>
</td>
<td align="left" width="63%">
Gets the host name for the content source, if applicable.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-getlastmodified">GetLastModified</a>
</td>
<td align="left" width="63%">
Gets the time stamp identifying when the URL was last modified.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-getredirectedurl">GetRedirectedURL</a>
</td>
<td align="left" width="63%">
Gets the redirected URL for the current item.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-getsecuritydescriptor">GetSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Gets the security descriptor for the URL item. Security is applied at query time, so this descriptor identifies security for read access.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-getsecurityprovider">GetSecurityProvider</a>
</td>
<td align="left" width="63%">
Gets the security provider for the URL. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Gets the size of the content designated by the URL.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-isdirectory">IsDirectory</a>
</td>
<td align="left" width="63%">
Ascertains whether the item URL points to a directory.
        

</td>
</tr>
</table> 


## -remarks



This is the main interface for pulling data from the content source. The Get... methods are for properties that are required by or useful to the filter host. Not all data sources have these properties. If the property returned by one of these methods is not meaningful for your data source, your protocol handler should return E_NOTIMPL.

The Bind... methods provide access to the data.

Although the protocol handler runs in the protocol host's multithreaded environment, each protocol handler runs in its own thread, employing one <b>IUrlAccessor</b> object at a time.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor2">IUrlAccessor2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor3">IUrlAccessor3</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-prth-error-constants">Search Protocol Handler Error Messages</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-indexing-process-overview">The Indexing Process</a>
 

 


---
UID: NN:searchapi.IUrlAccessor
title: IUrlAccessor
author: windows-driver-content
description: Provides methods for processing an individual item in a content source whose URL is provided by the gatherer to the filter host.
old-location: search\_search_IUrlAccessor.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\iurlaccessor.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IUrlAccessor, IUrlAccessor interface [search], IUrlAccessor interface [search], described, _search_IUrlAccessor, search._search_IUrlAccessor, searchapi/IUrlAccessor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	IUrlAccessor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IUrlAccessor interface


## -description


Provides methods for processing an individual item in a content source whose URL is provided by the gatherer to the filter host.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUrlAccessor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUrlAccessor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/282f13d8-8a68-4fcc-b2ff-1a5b0346918a">AddRequestParameter</a>
</td>
<td align="left" width="63%">

            Requests a property-value set. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9213766c-0e18-4b95-8535-b34e2e5dfa69">BindToFilter</a>
</td>
<td align="left" width="63%">

        Binds the item being processed to the appropriate <a href="https://msdn.microsoft.com/80b86ea0-d9d1-4d1f-b80f-90851e5bdf11">IFilter</a>and retrieves a pointer to the <b>IFilter</b>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02dc13c0-01a4-416d-ba14-c0390b4c4aae">BindToStream</a>
</td>
<td align="left" width="63%">

        Binds the item being processed to an <a href="_stg_istream">IStream interface [Structured Storage]</a> data stream and retrieves a pointer to that stream.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc56bacc-17a9-450f-a57c-22a90bde24b8">GetCLSID</a>
</td>
<td align="left" width="63%">

        Gets the <a href="_com_CLSID_Key">CLSID</a> for the document type of the URL item being processed.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2847de4b-79bb-4596-a0ed-fd494046aab4">GetDocFormat</a>
</td>
<td align="left" width="63%">

        Gets the document format, represented as a Multipurpose Internet Mail Extensions (MIME) string.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926842">GetFileName</a>
</td>
<td align="left" width="63%">

        Retrieves the file name of the item, which the filter host uses for indexing. If the item does not exist in a file system and the <a href="https://msdn.microsoft.com/02dc13c0-01a4-416d-ba14-c0390b4c4aae">IUrlAccessor::BindToStream</a> method is implemented, this method returns the shell's System.ParsingPath property for the item. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f411af30-bbc0-46d7-9504-44e8bd4e9ea0">GetHost</a>
</td>
<td align="left" width="63%">

         Gets the host name for the content source, if applicable.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/266d7eb8-fac6-410c-b733-07f69e7a1b35">GetLastModified</a>
</td>
<td align="left" width="63%">

        Gets the time stamp identifying when the URL was last modified.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d1e2a43-8d8f-444f-afcc-1e2da0d02563">GetRedirectedURL</a>
</td>
<td align="left" width="63%">

        Gets the redirected URL for the current item.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e63c00bf-dcc0-4245-b91d-183970b8e712">GetSecurityDescriptor</a>
</td>
<td align="left" width="63%">

            Gets the security descriptor for the URL item. Security is applied at query time, so this descriptor identifies security for read access.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36990eb7-3fdb-4e2f-810c-9469bf441b38">GetSecurityProvider</a>
</td>
<td align="left" width="63%">

            Gets the security provider for the URL. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15f11ad7-8727-4da1-b33f-9e5bb870813d">GetSize</a>
</td>
<td align="left" width="63%">

        Gets the size of the content designated by the URL.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b41a3d7-7d82-4f3c-8c43-db906a64c42d">IsDirectory</a>
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



<a href="https://msdn.microsoft.com/b4e6eb77-6cc3-48db-8b2a-4f7a3a052e49">IUrlAccessor2</a>



<a href="https://msdn.microsoft.com/4e13a780-b264-4baa-a7b5-a5736f2004f8">IUrlAccessor3</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/b5e99ad1-1698-483c-8173-796af33085c4">Search Protocol Handler Error Messages</a>



<a href="https://msdn.microsoft.com/cfba12eb-4123-4b57-8311-d4fc8f9f514e">The Indexing Process</a>
 

 


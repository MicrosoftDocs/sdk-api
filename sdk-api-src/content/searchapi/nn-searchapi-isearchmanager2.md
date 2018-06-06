---
UID: NN:searchapi.ISearchManager2
title: ISearchManager2
author: windows-sdk-content
description: Enabled applications to create and delete custom catalogs in the Windows Search indexer.
old-location: search\isearchmanager2.htm
old-project: search
ms.assetid: EE08AC43-D2E9-4B70-BBA5-52E36DD7F9A1
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ISearchManager2, ISearchManager2 interface [search], ISearchManager2 interface [search],described, search.isearchmanager2, searchapi/ISearchManager2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - searchapi.h
api_name:
 - ISearchManager2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISearchManager2 interface


## -description


Enabled applications to create and delete custom catalogs in the Windows Search indexer


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchManager2</b> interface inherits from <a href="https://msdn.microsoft.com/23aeb0f6-857e-490c-9ede-11c0955a45c9">ISearchManager</a>. <b>ISearchManager2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchManager2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ADC48B8-87A2-4527-9AA8-9B0BA3A12462">CreateCatalog</a>
</td>
<td align="left" width="63%">
Creates a new custom catalog in the Windows Search indexer and returns a reference to it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E9515AEE-6854-4FF8-9A83-10E6BC247D4D">DeleteCatalog</a>
</td>
<td align="left" width="63%">
Deletes an existing catalog and all associated indexed data from the Windows Search indexer.

</td>
</tr>
</table> 


## -remarks



ISearchManager interface ref: http://msdn.microsoft.com/en-us/library/bb231485(VS.85).aspx
Managing the Index ref: http://msdn.microsoft.com/en-us/library/bb266516(VS.85).aspx

The new functionality is exposed through the new ISearchManager2 interface. Apps can call QueryInterface on the existing ISearchManager interface to get the new interface. On older versions of Windows where this functionality does not exist the QueryInterface call will fail, and not return the new interface. The existing ISearchManager interface can be used unchanged.

Errors are returned through HRESULTs returned on each method in the standard way COM. ISupportErrorInfo / IErrorInfo are not supported. No exceptions are thrown.

These methods can be called in any COM apartment, and the behavior will not be impacted by the type of apartment. These APIs is safe to call on a UI thread but this is not recommended practice as the APIs involve cross-process IO and other potentially long-running operations.




## -see-also




<a href="https://msdn.microsoft.com/23aeb0f6-857e-490c-9ede-11c0955a45c9">ISearchManager</a>
 

 


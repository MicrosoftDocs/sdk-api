---
UID: NN:mswmdm.IWMDMStorage4
title: IWMDMStorage4 (mswmdm.h)
author: windows-sdk-content
description: The IWMDMStorage4 interface extends IWMDMStorage3 by providing methods for retrieving a subset of available metadata for a storage, and for setting and retrieving a list of references to other storages.
old-location: wmdm\iwmdmstorage4.htm
tech.root: WMDM
ms.assetid: ac80cc08-0ff0-48ee-b9c6-e094f803b751
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMDMStorage4, IWMDMStorage4 interface [windows Media Device Manager], IWMDMStorage4 interface [windows Media Device Manager],described, IWMDMStorage4Interface, mswmdm/IWMDMStorage4, wmdm.iwmdmstorage4
ms.topic: interface
f1_keywords: 
 - "mswmdm/IWMDMStorage4"
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - mswmdm.h
api_name:
 - IWMDMStorage4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMStorage4 interface


## -description



The <b>IWMDMStorage4</b> interface extends <b>IWMDMStorage3</b> by providing methods for retrieving a subset of available metadata for a storage, and for setting and retrieving a list of references to other storages.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMStorage4</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3">IWMDMStorage3</a>. <b>IWMDMStorage4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMStorage4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-findstorage">FindStorage</a>
</td>
<td align="left" width="63%">
Retrieves a storage in the current root storage by its unique identification (ID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getparent">GetParent</a>
</td>
<td align="left" width="63%">
Retrieves the parent of the storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getreferences">GetReferences</a>
</td>
<td align="left" width="63%">
Retrieves an array of pointers to <b>IWMDMStorage</b> pointed to by this storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getrightswithprogress">GetRightsWithProgress</a>
</td>
<td align="left" width="63%">
Retrieves the rights information for the storage object, providing a callback mechanism for monitoring progress.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata">GetSpecifiedMetadata</a>
</td>
<td align="left" width="63%">
Retrieves one or more specific metadata properties from the storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences">SetReferences</a>
</td>
<td align="left" width="63%">
Sets the references contained in a storage that has references (such as a playlist or album), overwriting any previously existing references held by the storage.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2">IWMDMStorage2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3">IWMDMStorage3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 


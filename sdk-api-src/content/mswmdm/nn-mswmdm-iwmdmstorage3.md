---
UID: NN:mswmdm.IWMDMStorage3
title: IWMDMStorage3 (mswmdm.h)

description: The IWMDMStorage3 interface extends IWMDMStorage2 by exposing metadata.
old-location: wmdm\iwmdmstorage3.htm
tech.root: WMDM
ms.assetid: b62ea18b-c692-464f-a009-727a2924f8b8

ms.date: 12/05/2018
ms.keywords: IWMDMStorage3, IWMDMStorage3 interface [windows Media Device Manager], IWMDMStorage3 interface [windows Media Device Manager],described, IWMDMStorage3Interface, mswmdm/IWMDMStorage3, wmdm.iwmdmstorage3
ms.topic: interface
f1_keywords: 
 - "mswmdm/IWMDMStorage3"
dev_langs:
 - c++
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
 - IWMDMStorage3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMStorage3 interface


## -description



The <b>IWMDMStorage3</b> interface extends <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2">IWMDMStorage2</a> by exposing metadata.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMStorage3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2">IWMDMStorage2</a>. <b>IWMDMStorage3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMStorage3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject">CreateEmptyMetadataObject</a>
</td>
<td align="left" width="63%">
Creates an object that supports the <b>IWMDMMetaData</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata">GetMetadata</a>
</td>
<td align="left" width="63%">
Retrieves the metadata associated with the storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference">SetEnumPreference</a>
</td>
<td align="left" width="63%">
Sets the preferred enumeration mode for the storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata">SetMetadata</a>
</td>
<td align="left" width="63%">
Sets metadata on the storage object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata">IWMDMMetaData Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2">IWMDMStorage2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 


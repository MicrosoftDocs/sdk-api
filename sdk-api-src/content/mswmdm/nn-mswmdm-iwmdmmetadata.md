---
UID: NN:mswmdm.IWMDMMetaData
title: IWMDMMetaData (mswmdm.h)
author: windows-sdk-content
description: The IWMDMMetaData interface sets and retrieves metadata properties (such as artist, album, genre, and so on) of a storage.
old-location: wmdm\iwmdmmetadata.htm
tech.root: WMDM
ms.assetid: ea57a851-0b9f-444c-9819-a278f2ece2b0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMDMMetaData, IWMDMMetaData interface [windows Media Device Manager], IWMDMMetaData interface [windows Media Device Manager],described, IWMDMMetaDataInterface, mswmdm/IWMDMMetaData, wmdm.iwmdmmetadata
ms.topic: interface
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
 - IWMDMMetaData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMMetaData interface


## -description



The <b>IWMDMMetaData</b> interface sets and retrieves metadata properties (such as artist, album, genre, and so on) of a storage. Metadata properties are stored as name-value pairs.

To create a new, empty instance of this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject">IWMDMStorage3::CreateEmptyMetadataObject</a>. To retrieve this interface (with values), call <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata">IWMDMStorage3::GetMetadata</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata">IWMDMStorage4::GetSpecifiedMetadata</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMMetaData</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMMetaData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMMetaData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem">AddItem</a>
</td>
<td align="left" width="63%">
Adds a metadata property to the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-getitemcount">GetItemCount</a>
</td>
<td align="left" width="63%">
Retrieves the total number of properties held by the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-querybyindex">QueryByIndex</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property specified by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-querybyname">QueryByName</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property specified by name.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/metadata-constants">Metadata Constants</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/setting-metadata-on-a-file">Setting Metadata on a File</a>
 

 


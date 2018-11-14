---
UID: NF:contentpartner.IWMPContentPartner.GetCatalogURL
title: IWMPContentPartner::GetCatalogURL
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentpartner_getcatalogurl.htm
tech.root: WMP
ms.assetid: 291440d5-b6d3-4586-98d2-3f7c56da29aa
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetCatalogURL, GetCatalogURL method [Windows Media Player], GetCatalogURL method [Windows Media Player],IWMPContentPartner interface, IWMPContentPartner interface [Windows Media Player],GetCatalogURL method, IWMPContentPartner.GetCatalogURL, IWMPContentPartner::GetCatalogURL, IWMPContentPartnerGetCatalogURL, contentpartner/IWMPContentPartner::GetCatalogURL, wmp.iwmpcontentpartner_getcatalogurl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: contentpartner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
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
 - contentpartner.h
api_name:
 - IWMPContentPartner.GetCatalogURL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- contentpartner.h
: 
- IWMPContentPartner.GetCatalogURL
: 
---

# IWMPContentPartner::GetCatalogURL


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetCatalogURL</b> method retrieves the URL from which to retrieve an update to the online store's current catalog.




## -parameters




### -param dwCatalogVersion [in]

<b>DWORD</b> containing the current catalog version.


### -param dwCatalogSchemaVersion [in]

<b>DWORD</b> containing the current catalog schema version.


### -param catalogLCID [in]

The locale ID (LCID) for the catalog.


### -param pdwNewCatalogVersion [out]

Address of a <b>DWORD</b> that receives the new catalog version.


### -param pbstrCatalogURL [out]

Address of a <b>BSTR</b> that receives the URL.


### -param pExpirationDate [out]

Address of a <b>VARIANT</b> (<b>VT_DATE</b>) that receives the expiration date of the catalog update.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



We recommend that the catalog URL specify the version as part of the path. For example, http://www.contoso.com/Catalogs/210/catalog.wmdb.




## -see-also




<a href="https://msdn.microsoft.com/49c03d3b-3381-4663-83c8-5bc8fa70f7c3">Catalog Compiler for Type 1 Online Stores</a>



<a href="https://msdn.microsoft.com/2078ebd4-3570-4c39-9081-1b55d9e8286f">IWMPContentPartner Interface</a>



<a href="https://msdn.microsoft.com/d7ebf37f-00ae-4978-a63d-9d13741724f5">Music Catalog</a>
 

 


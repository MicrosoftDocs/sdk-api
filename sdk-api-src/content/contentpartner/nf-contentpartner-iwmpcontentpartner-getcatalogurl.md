---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 


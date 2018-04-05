---
UID: NF:mfidl.IMFMetadata.DeleteProperty
title: IMFMetadata::DeleteProperty method
author: windows-driver-content
description: Deletes a metadata property.
old-location: mf\imfmetadata_deleteproperty.htm
old-project: medfound
ms.assetid: 7c9a406d-6144-4e9c-b62c-1d9c691391f0
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: 7c9a406d-6144-4e9c-b62c-1d9c691391f0, DeleteProperty method [Media Foundation], DeleteProperty method [Media Foundation], IMFMetadata interface, DeleteProperty,IMFMetadata.DeleteProperty, IMFMetadata, IMFMetadata interface [Media Foundation], DeleteProperty method, IMFMetadata::DeleteProperty, mf.imfmetadata_deleteproperty, mfidl/IMFMetadata::DeleteProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFMetadata.DeleteProperty
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMetadata::DeleteProperty method


## -description



          Deletes a metadata property.


## -parameters




### -param pwszName [in]

Pointer to a null-terminated string containing the name of the property.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_PROPERTY_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">

                The property was not found.
              

</td>
</tr>
</table>
 




## -remarks



For a media source, deleting a property from the metadata collection does not change the original content.




## -see-also




<a href="https://msdn.microsoft.com/411658ca-dc5e-445b-8d61-0c0429fcfbb1">IMFMetadata</a>



<a href="https://msdn.microsoft.com/dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9">Media Metadata</a>
 

 


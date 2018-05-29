---
UID: NF:mfidl.IMFMetadata.GetProperty
title: IMFMetadata::GetProperty
author: windows-sdk-content
description: Gets the value of a metadata property.
old-location: mf\imfmetadata_getproperty.htm
old-project: medfound
ms.assetid: 177c8612-5c9f-4a71-9ee1-a4c67737af2d
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 177c8612-5c9f-4a71-9ee1-a4c67737af2d, GetProperty, GetProperty method [Media Foundation], GetProperty method [Media Foundation],IMFMetadata interface, IMFMetadata interface [Media Foundation],GetProperty method, IMFMetadata.GetProperty, IMFMetadata::GetProperty, mf.imfmetadata_getproperty, mfidl/IMFMetadata::GetProperty
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFMetadata.GetProperty
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMetadata::GetProperty


## -description



          Gets the value of a metadata property.


## -parameters




### -param pwszName [in]


            A pointer to a null-terminated string that containings the name of the property.
          To get the list of property names, call <a href="https://msdn.microsoft.com/e0944d42-d6e6-420d-9980-ca6c62736b3d">IMFMetadata::GetAllPropertyNames</a>.


### -param ppvValue [out]


            Pointer to a <b>PROPVARIANT</b> that receives the value of the property. The <b>PROPVARIANT</b> type depends on the property. For multivalued properties, the <b>PROPVARIANT</b> is a <b>VT_VECTOR</b> type. The caller must free the <b>PROPVARIANT</b> by calling <a href="https://msdn.microsoft.com/062b6065-a56f-4ecd-b232-3ba338a6d806">PropVariantClear</a>.
          


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

                The requested property was not found.
              

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/411658ca-dc5e-445b-8d61-0c0429fcfbb1">IMFMetadata</a>



<a href="https://msdn.microsoft.com/dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9">Media Metadata</a>
 

 


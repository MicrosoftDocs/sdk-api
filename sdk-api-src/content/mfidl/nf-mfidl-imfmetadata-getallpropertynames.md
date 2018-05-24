---
UID: NF:mfidl.IMFMetadata.GetAllPropertyNames
title: IMFMetadata::GetAllPropertyNames
author: windows-driver-content
description: Gets a list of all the metadata property names on this object.
old-location: mf\imfmetadata_getallpropertynames.htm
old-project: medfound
ms.assetid: e0944d42-d6e6-420d-9980-ca6c62736b3d
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetAllPropertyNames, GetAllPropertyNames method [Media Foundation], GetAllPropertyNames method [Media Foundation],IMFMetadata interface, IMFMetadata interface [Media Foundation],GetAllPropertyNames method, IMFMetadata.GetAllPropertyNames, IMFMetadata::GetAllPropertyNames, e0944d42-d6e6-420d-9980-ca6c62736b3d, mf.imfmetadata_getallpropertynames, mfidl/IMFMetadata::GetAllPropertyNames
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
-	IMFMetadata.GetAllPropertyNames
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMetadata::GetAllPropertyNames


## -description



          Gets a list of all the metadata property names on this object.


## -parameters




### -param ppvNames [out]

Pointer to a <b>PROPVARIANT</b> that receives an array of null-terminated wide-character strings. If no properties are available, the <b>PROPVARIANT</b> type is VT_EMPTY. Otherwise, the <b>PROPVARIANT</b> type is VT_VECTOR | VT_LPWSTR. The caller must free the <b>PROPVARIANT</b> by calling <a href="https://msdn.microsoft.com/062b6065-a56f-4ecd-b232-3ba338a6d806">PropVariantClear</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/411658ca-dc5e-445b-8d61-0c0429fcfbb1">IMFMetadata</a>



<a href="https://msdn.microsoft.com/dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9">Media Metadata</a>
 

 


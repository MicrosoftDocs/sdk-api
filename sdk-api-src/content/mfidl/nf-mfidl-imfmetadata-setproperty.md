---
UID: NF:mfidl.IMFMetadata.SetProperty
title: IMFMetadata::SetProperty
author: windows-sdk-content
description: Sets the value of a metadata property.
old-location: mf\imfmetadata_setproperty.htm
tech.root: medfound
ms.assetid: 416a7fba-506c-405d-a230-7e8a1c801209
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: 416a7fba-506c-405d-a230-7e8a1c801209, IMFMetadata interface [Media Foundation],SetProperty method, IMFMetadata.SetProperty, IMFMetadata::SetProperty, SetProperty, SetProperty method [Media Foundation], SetProperty method [Media Foundation],IMFMetadata interface, mf.imfmetadata_setproperty, mfidl/IMFMetadata::SetProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMetadata.SetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMetadata::SetProperty


## -description


Sets the value of a metadata property.
        


## -parameters




### -param pwszName [in]

Pointer to a null-terminated string containing the name of the property.


### -param ppvValue [in]

Pointer to a <b>PROPVARIANT</b> that contains the value of the property. For multivalued properties, use a <b>PROPVARIANT</b> with a VT_VECTOR type.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/411658ca-dc5e-445b-8d61-0c0429fcfbb1">IMFMetadata</a>



<a href="https://msdn.microsoft.com/dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9">Media Metadata</a>
 

 


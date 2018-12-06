---
UID: NE:mfidl.MF_OBJECT_TYPE
title: MF_OBJECT_TYPE
author: windows-sdk-content
description: Defines the object types that are created by the source resolver.
old-location: mf\mf_object_type.htm
tech.root: medfound
ms.assetid: e919ae78-e3a5-42c5-b4e0-186e7e4fe54a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MF_OBJECT_BYTESTREAM, MF_OBJECT_INVALID, MF_OBJECT_MEDIASOURCE, MF_OBJECT_TYPE, MF_OBJECT_TYPE enumeration [Media Foundation], e919ae78-e3a5-42c5-b4e0-186e7e4fe54a, mf.mf_object_type, mfidl/MF_OBJECT_BYTESTREAM, mfidl/MF_OBJECT_INVALID, mfidl/MF_OBJECT_MEDIASOURCE, mfidl/MF_OBJECT_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MF_OBJECT_TYPE
product: Windows
targetos: Windows
req.typenames: MF_OBJECT_TYPE
req.redist: 
---

# MF_OBJECT_TYPE enumeration


## -description



Defines the object types that are created by the source resolver.




## -enum-fields




### -field MF_OBJECT_MEDIASOURCE

Media source. You can query the object for the <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> interface.


### -field MF_OBJECT_BYTESTREAM

Byte stream. You can query the object for the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface.


### -field MF_OBJECT_INVALID

Invalid type.


## -see-also




<a href="https://msdn.microsoft.com/079c61c5-7a29-4411-840e-9349190726ac">IMFSourceResolver</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/93eecf10-308b-4bb4-92f9-fd32d6ecdb04">Source Resolver</a>
 

 


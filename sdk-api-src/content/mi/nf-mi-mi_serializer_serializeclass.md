---
UID: NF:mi.MI_Serializer_SerializeClass
title: MI_Serializer_SerializeClass function
author: windows-sdk-content
description: Serializes an MI_Class into a buffer in the format specified when the serializer was created. Options can be passed into the flags to control if the class and all its parent classes are serialized, or just the child-most class.
old-location: wmi_v2\mi_serializer_serializeclass.htm
tech.root: WMI_v2
ms.assetid: 3417731d-8727-4dcb-8ce4-2b07b6addd19
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MI_Serializer_SerializeClass, MI_Serializer_SerializeClass function [Windows Management Infrastructure (MI)], mi/MI_Serializer_SerializeClass, wmi_v2.mi_serializer_serializeclass
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
 - Mi.h
api_name:
 - MI_Serializer_SerializeClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
- apiref
: 
- 
: 
- MI_Serializer_SerializeClass
: 
---

# MI_Serializer_SerializeClass function


## -description


Serializes an <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> into a buffer in the format specified when the serializer was created.  Options can be passed into the flags to control if the class and all its parent classes are serialized, or just the child-most class.


## -parameters




### -param serializer [in, out]

Serializer returned from <a href="https://msdn.microsoft.com/9de29d43-0677-4dc9-927f-af7c01179991">MI_Application_NewSerializer</a>.


### -param flags

Must be either 0 or <b>MI_SERIALIZER_FLAGS_CLASS_DEEP</b>. 0 means only the child most part of the class will be serialized. <b>MI_SERIALIZER_FLAGS_CLASS_DEEP</b> means all properties in the class will be serialized.


### -param classObject [in]

Class object to be serialized.


### -param clientBuffer

The output buffer to receive the serialized class data.  If this parameter is <b>Null</b>, the required length of the buffer is passed back in <i>clientBufferNeeded</i>.


### -param clientBufferLength

Length of the <i>clientBuffer</i> passed in.  If <i>clientBuffer</i> is <b>Null</b>, this parameter should be 0.


### -param clientBufferNeeded [in, out]

Returned total length the buffer needs to be.  If a buffer is passed in (via the <i>clientBuffer</i> parameter) that is the required size or more, this value will indicate how much buffer was used.  If a buffer was not passed in (where the <i>clientBuffer</i> value is <b>Null</b>) or the buffer is too small to hold the serialized class, this value will indicate how much space is needed to hold the serialized class.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/9de29d43-0677-4dc9-927f-af7c01179991">MI_Application_NewSerializer</a>
 

 


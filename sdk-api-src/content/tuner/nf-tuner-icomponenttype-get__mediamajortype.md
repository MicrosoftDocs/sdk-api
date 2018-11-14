---
UID: NF:tuner.IComponentType.get__MediaMajorType
title: IComponentType::get__MediaMajorType
author: windows-sdk-content
description: The get__MediaMajorType method retrieves the DirectShow media format type as a GUID.
old-location: mstv\icomponenttype_get__mediamajortype.htm
tech.root: MSTV
ms.assetid: b8732070-3560-461b-a04e-3c00d6b7b49e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],get__MediaMajorType method, IComponentType.get__MediaMajorType, IComponentType::get__MediaMajorType, IComponentTypeget__MediaMajorType, get__MediaMajorType, get__MediaMajorType method [Microsoft TV Technologies], get__MediaMajorType method [Microsoft TV Technologies],IComponentType interface, mstv.icomponenttype_get__mediamajortype, tuner/IComponentType::get__MediaMajorType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - IComponentType.get__MediaMajorType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tuner.h
: 
- IComponentType.get__MediaMajorType
: 
---

# IComponentType::get__MediaMajorType


## -description



The <b>get__MediaMajorType</b> method retrieves the DirectShow media format type as a GUID.




## -parameters




### -param MediaMajorTypeGuid

TBD




#### - MediaMajorType [out]

Pointer to a GUID that will receive the major type.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method is available through C++ only. Note the two underscores in the method name as compared to the one underscore for the method that uses a <b>BSTR</b> as a parameter.




## -see-also




<a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a>



<a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType Interface</a>
 

 


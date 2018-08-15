---
UID: NF:tuner.IComponentType.get__MediaSubType
title: IComponentType::get__MediaSubType
author: windows-sdk-content
description: The get__MediaSubType method retrieves the DirectShow media subtype as a GUID.
old-location: mstv\icomponenttype_get__mediasubtype.htm
old-project: mstv
ms.assetid: 92c49f9a-2102-424d-b04c-68aae8a37ada
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],get__MediaSubType method, IComponentType.get__MediaSubType, IComponentType::get__MediaSubType, IComponentTypeget__MediaSubType, get__MediaSubType, get__MediaSubType method [Microsoft TV Technologies], get__MediaSubType method [Microsoft TV Technologies],IComponentType interface, mstv.icomponenttype_get__mediasubtype, tuner/IComponentType::get__MediaSubType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IComponentType.get__MediaSubType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponentType::get__MediaSubType


## -description



The <b>get__MediaSubType</b> method retrieves the DirectShow media subtype as a GUID.




## -parameters




### -param MediaSubTypeGuid






#### - pMediaSubType [out]

Pointer to a GUID that will receive the major type.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method is available through C++ only. Note the two underscores in the method name as compared to the one underscore for the method that uses a <b>BSTR</b> as a parameter.




## -see-also




<a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a>



<a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType Interface</a>
 

 


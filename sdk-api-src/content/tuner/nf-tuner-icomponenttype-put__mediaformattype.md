---
UID: NF:tuner.IComponentType.put__MediaFormatType
title: IComponentType::put__MediaFormatType
author: windows-sdk-content
description: The put__MediaFormatType method sets the DirectShow media format type.
old-location: mstv\icomponenttype_put__mediaformattype.htm
tech.root: MSTV
ms.assetid: 37baa69e-d942-41d6-b497-bf37d6b0d57b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],put__MediaFormatType method, IComponentType.put__MediaFormatType, IComponentType::put__MediaFormatType, IComponentTypeput__MediaFormatType, mstv.icomponenttype_put__mediaformattype, put__MediaFormatType, put__MediaFormatType method [Microsoft TV Technologies], put__MediaFormatType method [Microsoft TV Technologies],IComponentType interface, tuner/IComponentType::put__MediaFormatType
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
 - IComponentType.put__MediaFormatType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComponentType::put__MediaFormatType


## -description



The <b>put__MediaFormatType</b> method sets the DirectShow media format type.




## -parameters




### -param MediaFormatTypeGuid

TBD




#### - MediaFormatType [in]

<b>REFCLSID</b> that specifies the media format type.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method is available through C++ only. Note the two underscores in the method name as compared to the one underscore for the method that uses a <b>BSTR</b> as a parameter.




## -see-also




<a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a>



<a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType Interface</a>
 

 


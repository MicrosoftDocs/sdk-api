---
UID: NE:codecapi.eAVEncMPVQScaleType
title: eAVEncMPVQScaleType (codecapi.h)
author: windows-sdk-content
description: Specifies whether the quantizer scale is linear or non-linear. This enumeration is used with the AVEncMPVQScaleType property.
old-location: dshow\eavencmpvqscaletype.htm
tech.root: DirectShow
ms.assetid: cc36ac03-66cb-4855-acf5-5f67265376b7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncMPVQScaleType, codecapi/eAVEncMPVQScaleType_Auto, codecapi/eAVEncMPVQScaleType_Linear, codecapi/eAVEncMPVScanPattern_AlternateScan, dshow.eavencmpvqscaletype, eAVEncMPVQScaleType, eAVEncMPVQScaleType enumeration [DirectShow], eAVEncMPVQScaleTypeEnumeration, eAVEncMPVQScaleType_Auto, eAVEncMPVQScaleType_Linear, eAVEncMPVScanPattern_AlternateScan
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - codecapi.h
api_name:
 - eAVEncMPVQScaleType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# eAVEncMPVQScaleType enumeration


## -description



Specifies whether the quantizer scale is linear or non-linear. This enumeration is used with the <a href="https://msdn.microsoft.com/0d1a62a2-7595-4c10-a1cf-d32dda337ecd">AVEncMPVQScaleType</a> property.




## -enum-fields




### -field eAVEncMPVQScaleType_Auto

The encoder selects the quantization scale.


### -field eAVEncMPVQScaleType_Linear

The quantization scale is linear.


### -field eAVEncMPVQScaleType_NonLinear




#### - eAVEncMPVScanPattern_AlternateScan

The quantization scale is non-linear.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd311953(v=VS.85).aspx">ICodecAPI Interface</a>
 

 


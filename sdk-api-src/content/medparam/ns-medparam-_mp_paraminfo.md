---
UID: NS:medparam._MP_PARAMINFO
title: "_MP_PARAMINFO"
author: windows-sdk-content
description: The MP_PARAMINFO structure contains information about a parameter.
old-location: dshow\mp_paraminfo.htm
old-project: DirectShow
ms.assetid: 91d2d08b-a55e-492f-a509-9c080cc438df
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: MP_PARAMINFO, MP_PARAMINFO structure [DirectShow], MP_PARAMINFOStructure, _MP_PARAMINFO, dshow.mp_paraminfo, medparam/MP_PARAMINFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: medparam.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MP_PARAMINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Medparam.h
api_name:
 - MP_PARAMINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MP_PARAMINFO structure


## -description



The <code>MP_PARAMINFO</code> structure contains information about a parameter.




## -struct-fields




### -field mpType

Member of the <a href="https://msdn.microsoft.com/9c8851c7-1a72-4dfd-ba2f-e64d8e22f6dc">MP_TYPE</a> enumeration that specifies the valid data type for this parameter.


### -field mopCaps

Bitwise combination of one or more <a href="https://msdn.microsoft.com/6f3b7666-d245-41fc-b6e4-9e1ed264dfdc">Parameter Capabilities Flags</a> that specify which envelope curves are supported. For Boolean and enumeration parameters, only MP_CAPS_CURVE_JUMP is valid.


### -field mpdMinValue

Minimum value of the parameter. Used only for parameters with numeric values.


### -field mpdMaxValue

Maximum value of the parameter. Used only for parameters with numeric values.


### -field mpdNeutralValue

Default or "neutral" value of the parameter.


### -field szUnitText

NULL-terminated wide-character string that contains the name of the units for the parameter.


### -field szLabel

NULL-terminated wide-character string that contains the name of the parameter.


## -remarks



The <b>szUnitText</b> and <b>szLabel</b> members always contain English-language strings. For international support, use the <a href="https://msdn.microsoft.com/38ecde61-fd4a-4ba3-9cd4-d62a5aa55294">IMediaParamInfo::GetParamText</a> method.




## -see-also




<a href="https://msdn.microsoft.com/82c8ea74-1c5e-4370-9075-6db2ed6b2c91">DMO Structures</a>
 

 


---
UID: NS:medparam._MP_PARAMINFO
title: MP_PARAMINFO (medparam.h)
description: The MP_PARAMINFO structure contains information about a parameter.helpviewer_keywords: ["MP_PARAMINFO","MP_PARAMINFO structure [DirectShow]","MP_PARAMINFOStructure","dshow.mp_paraminfo","medparam/MP_PARAMINFO"]
old-location: dshow\mp_paraminfo.htm
tech.root: DirectShow
ms.assetid: 91d2d08b-a55e-492f-a509-9c080cc438df
ms.date: 12/05/2018
ms.keywords: MP_PARAMINFO, MP_PARAMINFO structure [DirectShow], MP_PARAMINFOStructure, dshow.mp_paraminfo, medparam/MP_PARAMINFO
f1_keywords:
- medparam/MP_PARAMINFO
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Medparam.h
api_name:
- MP_PARAMINFO
targetos: Windows
req.typenames: MP_PARAMINFO
req.redist: 
ms.custom: 19H1
---

# MP_PARAMINFO structure


## -description



The <code>MP_PARAMINFO</code> structure contains information about a parameter.




## -struct-fields




### -field mpType

Member of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/medparam/ne-medparam-mp_type">MP_TYPE</a> enumeration that specifies the valid data type for this parameter.


### -field mopCaps

Bitwise combination of one or more <a href="https://docs.microsoft.com/windows/desktop/DirectShow/parameter-capabilities-flags">Parameter Capabilities Flags</a> that specify which envelope curves are supported. For Boolean and enumeration parameters, only MP_CAPS_CURVE_JUMP is valid.


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



The <b>szUnitText</b> and <b>szLabel</b> members always contain English-language strings. For international support, use the <a href="https://docs.microsoft.com/windows/desktop/api/medparam/nf-medparam-imediaparaminfo-getparamtext">IMediaParamInfo::GetParamText</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dmo-structures">DMO Structures</a>
 

 


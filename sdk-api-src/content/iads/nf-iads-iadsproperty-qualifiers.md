---
UID: NF:iads.IADsProperty.Qualifiers
title: IADsProperty::Qualifiers
author: windows-sdk-content
description: Returns a collection of ADSI objects that describe additional qualifiers of this property.
old-location: adsi\iadsproperty_qualifiers.htm
old-project: ADSI
ms.assetid: 48645dda-ba1e-47fa-b483-120ba982451e
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IADsProperty interface [ADSI],Qualifiers method, IADsProperty.Qualifiers, IADsProperty::Qualifiers, Qualifiers, Qualifiers method [ADSI], Qualifiers method [ADSI],IADsProperty interface, _ds_iadsproperty_qualifiers, adsi.iadsproperty__qualifiers, adsi.iadsproperty_qualifiers, iads/IADsProperty::Qualifiers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsProperty.Qualifiers
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsProperty::Qualifiers


## -description


The <b>IADsProperty::Qualifiers</b> method is an optional method that returns a collection of ADSI objects that describe additional qualifiers of this property.


## -parameters




### -param ppQualifiers [out]

Indirect pointer to the  <a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a> interface on the ADSI collection object that represents additional limits for this property.


## -returns



This method supports the standard return values <b>E_FAIL</b> and <b>E_UNEXPECTED</b>, as well as the following:




## -remarks



The qualifier objects are provider-specific. When supported, this method can be used to obtain extended schema data.

This method is not currently supported by any of the providers supplied by Microsoft.




## -see-also




<a href="https://msdn.microsoft.com/d05e4278-2dfb-4832-a97d-eb35253ae535">IADsClass::Qualifiers</a>



<a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a>



<a href="https://msdn.microsoft.com/ebf03974-371b-4bf4-91b4-f137339bd784">IADsProperty</a>
 

 


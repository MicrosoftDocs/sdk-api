---
UID: NF:iads.IADsProperty.Qualifiers
title: IADsProperty::Qualifiers (iads.h)
description: Returns a collection of ADSI objects that describe additional qualifiers of this property.
old-location: adsi\iadsproperty_qualifiers.htm
tech.root: adsi
ms.assetid: 48645dda-ba1e-47fa-b483-120ba982451e
ms.date: 12/05/2018
ms.keywords: IADsProperty interface [ADSI],Qualifiers method, IADsProperty.Qualifiers, IADsProperty::Qualifiers, Qualifiers, Qualifiers method [ADSI], Qualifiers method [ADSI],IADsProperty interface, _ds_iadsproperty_qualifiers, adsi.iadsproperty__qualifiers, adsi.iadsproperty_qualifiers, iads/IADsProperty::Qualifiers
ms.topic: method
f1_keywords:
- iads/IADsProperty.Qualifiers
dev_langs:
- c++
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
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Activeds.dll
api_name:
- IADsProperty.Qualifiers
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsProperty::Qualifiers


## -description


The <b>IADsProperty::Qualifiers</b> method is an optional method that returns a collection of ADSI objects that describe additional qualifiers of this property.


## -parameters




### -param ppQualifiers [out]

Indirect pointer to the  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadscollection">IADsCollection</a> interface on the ADSI collection object that represents additional limits for this property.


## -returns



This method supports the standard return values <b>E_FAIL</b> and <b>E_UNEXPECTED</b>, as well as the following:




## -remarks



The qualifier objects are provider-specific. When supported, this method can be used to obtain extended schema data.

This method is not currently supported by any of the providers supplied by Microsoft.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsclass-qualifiers">IADsClass::Qualifiers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadscollection">IADsCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsproperty">IADsProperty</a>
 

 


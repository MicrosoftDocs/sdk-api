---
UID: NF:iads.IADsPropertyValue2.PutObjectProperty
title: IADsPropertyValue2::PutObjectProperty method
author: windows-driver-content
description: Sets an attribute value.
old-location: adsi\iadspropertyvalue2_putobjectproperty.htm
old-project: ADSI
ms.assetid: 53dad13f-7df7-4c1d-8c8a-946c291b20c6
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IADsPropertyValue2, IADsPropertyValue2 interface [ADSI], PutObjectProperty method, IADsPropertyValue2::PutObjectProperty, PutObjectProperty method [ADSI], PutObjectProperty method [ADSI], IADsPropertyValue2 interface, PutObjectProperty,IADsPropertyValue2.PutObjectProperty, _ds_iadspropertyvalue2_putobjectproperty, adsi.iadspropertyvalue2__putobjectproperty, adsi.iadspropertyvalue2_putobjectproperty, iads/IADsPropertyValue2::PutObjectProperty
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Activeds.dll
api_name:
-	IADsPropertyValue2.PutObjectProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsPropertyValue2::PutObjectProperty method


## -description


The <b>IADsPropertyValue2::PutObjectProperty</b> method sets an attribute value.


## -parameters




### -param lnADsType [in]

Contains one of the <a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a> values that specifies the data format of the value set. This value must correspond to the <i>pvProp</i> variant type. For more information and a list of the <i>lnADsType</i> values and corresponding <i>pvProp</i> variant types, see <a href="https://msdn.microsoft.com/57a3b413-f658-4793-abad-358455b5b9f4">IADsPropertyValue2</a>.


### -param vProp






#### - pvProp [in]

Pointer to a <b>VARIANT</b> that contains the new attribute value. The variant type of this data must correspond to the value in <i>lnADsType</i>. For more information and a list of the <i>lnADsType</i> values and corresponding <i>pvProp</i> variant types, see <a href="https://msdn.microsoft.com/57a3b413-f658-4793-abad-358455b5b9f4">IADsPropertyValue2</a>.


## -returns



Returns <b>S_OK</b> if successful or an error code otherwise. The following are the most common error codes.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a>



<a href="https://msdn.microsoft.com/7cad4d04-80d4-4f9a-95b7-2f1809ddb8fb">IADsPropertyValue</a>



<a href="https://msdn.microsoft.com/57a3b413-f658-4793-abad-358455b5b9f4">IADsPropertyValue2</a>
 

 


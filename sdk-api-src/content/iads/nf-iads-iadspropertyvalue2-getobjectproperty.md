---
UID: NF:iads.IADsPropertyValue2.GetObjectProperty
title: IADsPropertyValue2::GetObjectProperty (iads.h)
author: windows-sdk-content
description: Retrieves an attribute value.
old-location: adsi\iadspropertyvalue2_getobjectproperty.htm
tech.root: adsi
ms.assetid: a189f106-23dc-441b-8d97-c03d4c49a4a1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetObjectProperty, GetObjectProperty method [ADSI], GetObjectProperty method [ADSI],IADsPropertyValue2 interface, IADsPropertyValue2 interface [ADSI],GetObjectProperty method, IADsPropertyValue2.GetObjectProperty, IADsPropertyValue2::GetObjectProperty, _ds_iadspropertyvalue2_getobjectproperty, adsi.iadspropertyvalue2__getobjectproperty, adsi.iadspropertyvalue2_getobjectproperty, iads/IADsPropertyValue2::GetObjectProperty
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
 - IADsPropertyValue2.GetObjectProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsPropertyValue2::GetObjectProperty


## -description


The <b>IADsPropertyValue2::GetObjectProperty</b> method retrieves an attribute value.


## -parameters




### -param lnADsType [in, out]

Pointer to a variable that, on entry, contains one of the <a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a> values that specifies the data format that the value should be returned.

If the data type is not known, set this to <b>ADSTYPE_UNKNOWN</b>. In this case, this method will obtain the attribute value in the default data type and set this variable to the corresponding <a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a> value. If any other <b>ADSTYPEENUM</b> value is specified, ADSI will return the attribute value only if the data type matches the format of the value.


### -param pvProp [out]

Pointer to a <b>VARIANT</b> that receives the requested attribute value. The variant type of this data will depend on the value returned in <i>lnADsType</i>. For more information and  a list of the <i>lnADsType</i> values and corresponding <i>pvProp</i> variant types, see <a href="https://msdn.microsoft.com/57a3b413-f658-4793-abad-358455b5b9f4">IADsPropertyValue2</a>.


## -returns



Returns <b>S_OK</b> if successful or one of the following error codes.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a>



<a href="https://msdn.microsoft.com/7cad4d04-80d4-4f9a-95b7-2f1809ddb8fb">IADsPropertyValue</a>



<a href="https://msdn.microsoft.com/57a3b413-f658-4793-abad-358455b5b9f4">IADsPropertyValue2</a>
 

 


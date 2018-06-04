---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 


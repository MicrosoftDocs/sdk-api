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

# EAP_METHOD_PROPERTY_VALUE structure


## -description


The <b>EAP_METHOD_PROPERTY_VALUE</b> union contains the value of an EAP method property.


## -struct-fields




### -field empvBool

case(<i>empvtBool</i>)

If  <a href="https://msdn.microsoft.com/df8c9ba2-e1c5-4011-bdbe-1d04765d19cd">eapMethodPropertyValueType</a> specifies a Boolean type (<i>empvtBool</i>), the data pointed to by this parameter is defined by the <a href="https://msdn.microsoft.com/ff482df6-a9c9-41b3-bedf-880fee71b968">EAP_METHOD_PROPERTY_VALUE_BOOL</a> structure.


### -field empvBool.case

 


### -field empvBool.case.empvtBool

 


### -field empvDword

case(<i>empvDword</i>)

If <a href="https://msdn.microsoft.com/df8c9ba2-e1c5-4011-bdbe-1d04765d19cd">eapMethodPropertyValueType</a> specifies a DWORD type (empvtDword), the data pointed to by this parameter is defined by the  <a href="https://msdn.microsoft.com/79a1ff42-dfd9-4408-b96c-2fbc33c2ca93">EAP_METHOD_PROPERTY_VALUE_DWORD</a> structure.


### -field empvDword.case

 


### -field empvDword.case.empvtDword

 


### -field empvString

case(<i>empvString</i>)

If <a href="https://msdn.microsoft.com/df8c9ba2-e1c5-4011-bdbe-1d04765d19cd">eapMethodPropertyValueType</a> specifies a BYTE *(empvtString), the data pointed to by this parameter is defined by the   <a href="https://msdn.microsoft.com/afb2d8f3-c2b1-45b8-9ff3-814c8e4b1595">EAP_METHOD_PROPERTY_VALUE_STRING</a> structure.


### -field empvString.case

 


### -field empvString.case.empvtString

 


### -field switch_type

 


### -field switch_type.EAP_METHOD_PROPERTY_VALUE_TYPE

 




## -see-also




<a href="https://msdn.microsoft.com/77595f36-140d-4d8e-af8e-63e9de0031c4">EAPHost Supplicant Structures</a>



<a href="https://msdn.microsoft.com/df8c9ba2-e1c5-4011-bdbe-1d04765d19cd">EAP_METHOD_PROPERTY</a>



<a href="https://msdn.microsoft.com/b553c022-c9a2-4cf7-8c09-e629b49cd929">EapHostPeerGetMethodProperties</a>
 

 


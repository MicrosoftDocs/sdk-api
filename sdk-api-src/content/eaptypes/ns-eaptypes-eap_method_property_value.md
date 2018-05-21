---
UID: NS:eaptypes.EAP_METHOD_PROPERTY_VALUE
title: EAP_METHOD_PROPERTY_VALUE
author: windows-driver-content
description: Contains the value of an EAP method property.
old-location: eaphost\eap_method_property_value.htm
old-project: EAPHost
ms.assetid: 298b59d3-245f-4a29-b8a1-2265d65d30e6
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: EAP_METHOD_PROPERTY_VALUE, EAP_METHOD_PROPERTY_VALUE union [EAPHost], eaphost.eap_method_property_value, eaptypes/EAP_METHOD_PROPERTY_VALUE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: eaptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EAP_METHOD_PROPERTY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	EapTypes.h
api_name:
-	EAP_METHOD_PROPERTY_VALUE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 


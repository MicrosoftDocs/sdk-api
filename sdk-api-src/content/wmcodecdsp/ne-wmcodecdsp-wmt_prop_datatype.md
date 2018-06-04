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

# WMT_PROP_DATATYPE enumeration


## -description


Defines the data types used for the codec and DSP properties that are accessed by using the methods of the <a href="https://msdn.microsoft.com/b49e506b-8c87-44b9-be6c-b9a33f6c9ecb">IWMCodecProps</a> interface.




## -enum-fields




### -field WMT_PROP_TYPE_DWORD

Specifies a double-word value.


### -field WMT_PROP_TYPE_STRING

Specifies a string value.


### -field WMT_PROP_TYPE_BINARY

Specifies a binary value.


### -field WMT_PROP_TYPE_BOOL

Specifies a Boolean value.


### -field WMT_PROP_TYPE_QWORD

Specifies a quadruple-word value.


### -field WMT_PROP_TYPE_WORD

Specifies a word value.


### -field WMT_PROP_TYPE_GUID

Specifies a GUID value.


## -remarks



Most properties are accessed by using the methods of the <b>IPropertyBag</b> interface. The data types of those properties are defined as constants used with <b>VARIANTARG</b> values.






## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 


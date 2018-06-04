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

# IWbemObjectTextSrc::GetText


## -description


The <b>IWbemObjectTextSrc::GetText</b> method creates a textual representation of an 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> object; for example, an XML representation.


## -parameters




### -param lFlags

Reserved. Must be 0L.


### -param pObj

Reference to the object to be represented in text format. This parameter cannot be <b>NULL</b>.


### -param uObjTextFormat

Definition of the text format used to represent the object. For more information about valid values for this parameter, see Remarks.



#### WMI_OBJ_TEXT_CIM_DTD_2_0 (1 (0x1))

Use the DTD that corresponds to CIM DTD version 2.0.



#### WMI_OBJ_TEXT_WMI_DTD_2_0 (2 (0x2))

Use the WMI DTD that corresponds to CIM DTD version 2.0. Using this value enables WMI-specific extensions, such as embedded objects or scope.



#### WMI_OBJ_TEXT_WMI_EXT1 (3 (0x3))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT2 (4 (0x4))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT3 (5 (0x5))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT4 (6 (0x6))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT5 (7 (0x7))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT6 (8 (0x8))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT7 (9 (0x9))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT8 (10 (0xA))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT9 (11 (0xB))

Reserved for future use.



#### WMI_OBJ_TEXT_WMI_EXT10 (12 (0xC))

Reserved for future use.



#### WMI_OBJ_TEXT_LAST (13 (0xD))

Reserved for future use.


### -param pCtx

Optional. Context object for the operation. The context object can be used to specify whether  certain parts of the object are represented in text; for example, whether to include qualifiers in the textual representation. The context object takes the following optional values.



#### LocalOnly (VT_BOOL)

If <b>TRUE</b>, only locally defined properties and methods are present in the resulting XML. The default is <b>FALSE</b>.



#### IncludeQualifiers (VT_BOOL)

If <b>TRUE</b>, the qualifiers of classes, instances, properties, and methods are included in the output. The default is <b>FALSE</b>.



#### PathLevel (VT_I4)

The default is 0 (zero).

Possible values are:

<ul>
<li>
0

A <b>CLASS</b> or <b>INSTANCE</b> element is created depending on whether the object is a class or instance.

</li>
<li>
1

A <b>VALUE.NAMEDOBJECT</b> element is generated.

</li>
<li>
2

A VALUE.<b>OBJECTWITHLOCALPATH</b> element is generated.

</li>
<li>
3

A <b>VALUE.OBJECTWITHPATH</b> element is generated.

</li>
</ul>


#### ExcludeSystemProperties (VT_BOOL)

If <b>TRUE</b>, system properties, like <a href="https://msdn.microsoft.com/d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc">__NAMESPACE</a>, are absent in the output. The default is <b>FALSE</b>.



#### IncludeClassOrigin (VT_BOOL)

If <b>TRUE</b>, the class origin attribute is set on <b>PROPERTY</b> and <b>METHOD</b> elements. The default is <b>FALSE</b>.


### -param strText

Textual representation of the object. User must free the string using <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> when finished with <i>strText</i>.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



For more information, see 
<a href="https://msdn.microsoft.com/06d2b532-7ab2-489d-9021-27b5187c8f2b">Representing Objects in XML</a>.




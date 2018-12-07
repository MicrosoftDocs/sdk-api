---
UID: NS:wsdxmldom._WSDXML_ATTRIBUTE
title: "_WSDXML_ATTRIBUTE"
author: windows-sdk-content
description: Describes an XML attribute.
old-location: ncd\wsdxml_attribute_struct.htm
tech.root: wsdapi
ms.assetid: 2697d30d-17c7-417d-a02b-c4427987ec4b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSDXML_ATTRIBUTE, WSDXML_ATTRIBUTE structure, _WSDXML_ATTRIBUTE, ncd.wsdxml_attribute_struct, wsdxmldom/WSDXML_ATTRIBUTE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wsdxmldom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - WsdXmldom.h
api_name:
 - WSDXML_ATTRIBUTE
product: Windows
targetos: Windows
req.typenames: WSDXML_ATTRIBUTE
req.redist: 
---

# _WSDXML_ATTRIBUTE structure


## -description


Describes an XML attribute.


## -struct-fields




### -field Element

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies parent element of the attribute.


### -field Next

Reference to a <b>WSDXML_ATTRIBUTE</b> structure that specifies the next sibling attribute, if any.


### -field Name

Reference to a <a href="https://msdn.microsoft.com/9dce71d2-700c-4f86-9308-dee6a69010bb">WSDXML_NAME</a> structure that specifies the qualified name of the attribute.


### -field Value

The value of the attribute.


## -remarks



<b>WSDXML_ATTRIBUTE</b> is used to describe attribute values in an XML element.




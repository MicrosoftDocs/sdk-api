---
UID: NF:pla.IValueMap.get_Value
title: IValueMap::get_Value method
author: windows-driver-content
description: Retrieves or sets the value of the collection.
old-location: pla\ivaluemap_value.htm
old-project: PLA
ms.assetid: 9f344845-956e-4254-82e2-e4e00f6a371b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IValueMap, IValueMap interface [PLA], Value property, IValueMap.Value, IValueMap::get_Value, IValueMap::put_Value, Value property [PLA], Value property [PLA], IValueMap interface, base.ivaluemap_value, get_Value,IValueMap.get_Value, pla.ivaluemap_value, pla/IValueMap::Value, pla/IValueMap::get_Value, pla/IValueMap::put_Value
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: pla.h
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
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IValueMap.Value
-	IValueMap.get_Value
-	IValueMap.put_Value
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IValueMap::get_Value method


## -description


Retrieves or sets the value of the collection.

This property is read/write.


## -parameters


## -remarks



Depending on the value of the <a href="https://msdn.microsoft.com/42cea1e6-c945-4bae-ac65-a052b4069e5f">IValueMap::ValueMapType</a> property, this value is either one of the values in the collection or the value derived by combining all the item values in the collection with the <b>OR</b> operator.

The variant type is VT_UI8 if the <a href="https://msdn.microsoft.com/cc217b3b-389a-4d15-b47d-456778f3eaec">ValueMapType</a> enumeration is <b>plaIndex</b>, <b>plaFlag</b> or <b>plaFlagArray</b>.

The variant type is VT_UI4 if the <a href="https://msdn.microsoft.com/cc217b3b-389a-4d15-b47d-456778f3eaec">ValueMapType</a> enumeration is <b>plaValidation</b>.




## -see-also




<a href="https://msdn.microsoft.com/a7134395-91c6-4ea1-8b76-63830048289f">IValueMap</a>



<a href="https://msdn.microsoft.com/42cea1e6-c945-4bae-ac65-a052b4069e5f">IValueMap::ValueMapType</a>
 

 


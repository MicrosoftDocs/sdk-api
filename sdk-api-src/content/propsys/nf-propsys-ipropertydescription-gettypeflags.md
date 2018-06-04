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

# IPropertyDescription::GetTypeFlags


## -description


Gets a set of flags that describe the uses and capabilities of the property.


## -parameters




### -param mask [in]

Type: <b><a href="shell.PROPDESC_TYPE_FLAGS">PROPDESC_TYPE_FLAGS</a></b>

A mask that specifies which type flags to retrieve. A combination of values found in the <a href="shell.PROPDESC_TYPE_FLAGS">PROPDESC_TYPE_FLAGS</a> constants. To retrieve all type flags, pass <a href="shell.PROPDESC_TYPE_FLAGS">PDTF_MASK_ALL</a>



### -param ppdtFlags






#### - ppdtfFlags [out]

Type: <b><a href="shell.PROPDESC_TYPE_FLAGS">PROPDESC_TYPE_FLAGS</a>*</b>

When this method returns, contains a pointer to a value that consists of bitwise <a href="shell.PROPDESC_TYPE_FLAGS">PROPDESC_TYPE_FLAGS</a> values.


## -returns



Type: <b>HRESULT</b>

Always returns <b>S_OK</b>.




## -remarks



If the property description instance comes from <a href="shell.PSGetPropertyDescription">PSGetPropertyDescription</a> or <a href="shell.PSGetPropertyDescriptionByName">PSGetPropertyDescriptionByName</a>, these flags come from the .propdesc file that defines the property description.

If the instance comes from <a href="https://msdn.microsoft.com/library/windows/hardware/hh406567">GetAt</a>, the type flags come from the .propdesc file and may be influenced by the specific proplist. This means that flags obtained from one property description instance may be slightly different from another instance (both referring to the same property).

For additional information on type flags, see the <i>canGroupBy</i>, <i>canStackBy</i>, <i>isInnate</i>, <i>multipleValues</i>, <i>isGroup</i>, <i>isTreeProperty</i>, <i>isViewable</i>, <i>isQueryable</i>, and <i>includeInFullTextQuery</i> attributes of the <a href="shell.propdesc_schema_typeInfo">typeInfo</a> element in the property's .propdesc file.




## -see-also




<a href="shell.IPropertyDescription">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 


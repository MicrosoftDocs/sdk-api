---
UID: NF:propsys.IPropertyDescription.GetTypeFlags
title: IPropertyDescription::GetTypeFlags
author: windows-sdk-content
description: Gets a set of flags that describe the uses and capabilities of the property.
old-location: properties\IPropertyDescription_GetTypeFlags.htm
old-project: properties
ms.assetid: 20ff02c1-72de-479f-afd8-29ec580bbfcb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetTypeFlags, GetTypeFlags method [Windows Properties], GetTypeFlags method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetTypeFlags method, IPropertyDescription.GetTypeFlags, IPropertyDescription::GetTypeFlags, properties.IPropertyDescription_GetTypeFlags, propsys/IPropertyDescription::GetTypeFlags, shell.IPropertyDescription_GetTypeFlags, shell_IPropertyDescription_GetTypeFlags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PSC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescription.GetTypeFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 


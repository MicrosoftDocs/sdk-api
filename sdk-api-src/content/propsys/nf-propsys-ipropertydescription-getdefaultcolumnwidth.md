---
UID: NF:propsys.IPropertyDescription.GetDefaultColumnWidth
title: IPropertyDescription::GetDefaultColumnWidth
author: windows-sdk-content
description: Gets the default column width of the property in a list view.
old-location: properties\IPropertyDescription_GetDefaultColumnWidth.htm
old-project: properties
ms.assetid: 3f39cb88-084b-4eca-8168-871dcdc74f98
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetDefaultColumnWidth, GetDefaultColumnWidth method [Windows Properties], GetDefaultColumnWidth method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetDefaultColumnWidth method, IPropertyDescription.GetDefaultColumnWidth, IPropertyDescription::GetDefaultColumnWidth, properties.IPropertyDescription_GetDefaultColumnWidth, propsys/IPropertyDescription::GetDefaultColumnWidth, shell.IPropertyDescription_GetDefaultColumnWidth, shell_IPropertyDescription_GetDefaultColumnWidth
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
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IPropertyDescription.GetDefaultColumnWidth
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPropertyDescription::GetDefaultColumnWidth


## -description


Gets the default column width of the property in a list view.


## -parameters




### -param pcxChars [out]

Type: <b>DWORD*</b>

A pointer to the column width value, in characters.


## -returns



Type: <b>HRESULT</b>

Always returns <b>S_OK</b>.




## -remarks



The values retrieved by this method are originally set through the <i>defaultColumnWidth</i> attribute of the <a href="shell.propdesc_schema_displayInfo">displayInfo</a> element in the property's .propdesc file.

If no value is set in the .propdesc file or if the method fails, the value pointed to by <i>pcxChars</i> is 20 characters.




## -see-also




<a href="shell.IPropertyDescription">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 


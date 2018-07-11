---
UID: NF:propsys.IPropertyDescription.GetRelativeDescriptionType
title: IPropertyDescription::GetRelativeDescriptionType
author: windows-sdk-content
description: Gets the relative description type for a property description.
old-location: properties\IPropertyDescription_GetRelativeDescriptionType.htm
old-project: properties
ms.assetid: b3778988-63ac-4827-8098-c3c5b6b13e38
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetRelativeDescriptionType, GetRelativeDescriptionType method [Windows Properties], GetRelativeDescriptionType method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetRelativeDescriptionType method, IPropertyDescription.GetRelativeDescriptionType, IPropertyDescription::GetRelativeDescriptionType, properties.IPropertyDescription_GetRelativeDescriptionType, propsys/IPropertyDescription::GetRelativeDescriptionType, shell.IPropertyDescription_GetRelativeDescriptionType, shell_IPropertyDescription_GetRelativeDescriptionType
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
 - IPropertyDescription.GetRelativeDescriptionType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPropertyDescription::GetRelativeDescriptionType


## -description


Gets the relative description type for a property description.


## -parameters




### -param prdt [out]

Type: <b><a href="shell.PROPDESC_RELATIVEDESCRIPTION_TYPE">PROPDESC_RELATIVEDESCRIPTION_TYPE</a>*</b>

When this method returns, contains a pointer to the relative description type value. See <a href="shell.PROPDESC_RELATIVEDESCRIPTION_TYPE">PROPDESC_RELATIVEDESCRIPTION_TYPE</a> for valid values.


## -returns



Type: <b>HRESULT</b>

Always returns <b>S_OK</b>.




## -remarks



The information retrieved by this method comes from the <i>relativeDescriptionType</i> attribute of the <a href="shell.propdesc_schema_displayInfo">displayInfo</a> element in the property's .propdesc file.




## -see-also




<a href="shell.IPropertyDescription">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 


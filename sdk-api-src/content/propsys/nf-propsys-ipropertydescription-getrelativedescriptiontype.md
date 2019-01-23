---
UID: NF:propsys.IPropertyDescription.GetRelativeDescriptionType
title: IPropertyDescription::GetRelativeDescriptionType
author: windows-sdk-content
description: Gets the relative description type for a property description.
old-location: properties\IPropertyDescription_GetRelativeDescriptionType.htm
tech.root: properties
ms.assetid: b3778988-63ac-4827-8098-c3c5b6b13e38
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRelativeDescriptionType, GetRelativeDescriptionType method [Windows Properties], GetRelativeDescriptionType method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetRelativeDescriptionType method, IPropertyDescription.GetRelativeDescriptionType, IPropertyDescription::GetRelativeDescriptionType, properties.IPropertyDescription_GetRelativeDescriptionType, propsys/IPropertyDescription::GetRelativeDescriptionType, shell.IPropertyDescription_GetRelativeDescriptionType, shell_IPropertyDescription_GetRelativeDescriptionType
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# IPropertyDescription::GetRelativeDescriptionType


## -description


Gets the relative description type for a property description.


## -parameters




### -param prdt [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb762526(v=VS.85).aspx">PROPDESC_RELATIVEDESCRIPTION_TYPE</a>*</b>

When this method returns, contains a pointer to the relative description type value. See <a href="https://msdn.microsoft.com/en-us/library/Bb762526(v=VS.85).aspx">PROPDESC_RELATIVEDESCRIPTION_TYPE</a> for valid values.


## -returns



Type: <b>HRESULT</b>

Always returns <b>S_OK</b>.




## -remarks



The information retrieved by this method comes from the <i>relativeDescriptionType</i> attribute of the <a href="https://msdn.microsoft.com/en-us/library/Bb773865(v=VS.85).aspx">displayInfo</a> element in the property's .propdesc file.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 


---
UID: NF:propsys.IPropertyDescriptionRelatedPropertyInfo.GetRelatedProperty
title: IPropertyDescriptionRelatedPropertyInfo::GetRelatedProperty
author: windows-sdk-content
description: Retrieves an IPropertyDescription object that represents the related property.
old-location: properties\IPropertyDescriptionRelatedPropertyInfo_GetRelatedProperty.htm
tech.root: properties
ms.assetid: 735880dc-4cf2-4f4a-b9fc-f4dddd19415d
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetRelatedProperty, GetRelatedProperty method [Windows Properties], GetRelatedProperty method [Windows Properties],IPropertyDescriptionRelatedPropertyInfo interface, IPropertyDescriptionRelatedPropertyInfo interface [Windows Properties],GetRelatedProperty method, IPropertyDescriptionRelatedPropertyInfo.GetRelatedProperty, IPropertyDescriptionRelatedPropertyInfo::GetRelatedProperty, _shell_IPropertyDescriptionRelatedPropertyInfo_GetRelatedProperty, properties.IPropertyDescriptionRelatedPropertyInfo_GetRelatedProperty, propsys/IPropertyDescriptionRelatedPropertyInfo::GetRelatedProperty, shell.IPropertyDescriptionRelatedPropertyInfo_GetRelatedProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IPropertyDescriptionRelatedPropertyInfo.GetRelatedProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyDescriptionRelatedPropertyInfo::GetRelatedProperty


## -description


Retrieves an <a href="shell.IPropertyDescription">IPropertyDescription</a> object that represents the related property.


## -parameters




### -param pszRelationshipName [in]

Type: <b>LPCWSTR</b>

A pointer to a string that contains the relationship of the property to get.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through the <i>ppv</i> parameter, typically IID_IPropertyDescription.


### -param ppv [out]

Type: <b>void**</b>

Receives the interface pointer requested in the parameter. This is typically <a href="shell.IPropertyDescription">IPropertyDescription</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



We recommend that you use the <a href="https://msdn.microsoft.com/268B59FA-44EB-4777-8162-C50981CBDD09">IID_PPV_ARGS</a> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.




## -see-also




<a href="shell.IPropertyDescriptionRelatedPropertyInfo">IPropertyDescriptionRelatedPropertyInfo</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 


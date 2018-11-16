---
UID: NF:propsys.IPropertyDescription.GetRelativeDescription
title: IPropertyDescription::GetRelativeDescription
author: windows-sdk-content
description: Compares two property values in the manner specified by the property description. Returns two display strings that describe how the two properties compare.
old-location: properties\IPropertyDescription_GetRelativeDescription.htm
tech.root: properties
ms.assetid: d98cc2de-8f1c-4827-99b9-2b770d1270e3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetRelativeDescription, GetRelativeDescription method [Windows Properties], GetRelativeDescription method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetRelativeDescription method, IPropertyDescription.GetRelativeDescription, IPropertyDescription::GetRelativeDescription, properties.IPropertyDescription_GetRelativeDescription, propsys/IPropertyDescription::GetRelativeDescription, shell.IPropertyDescription_GetRelativeDescription, shell_IPropertyDescription_GetRelativeDescription
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPropertyDescription.GetRelativeDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- propsys.h
: 
- IPropertyDescription.GetRelativeDescription
: 
---

# IPropertyDescription::GetRelativeDescription


## -description


Compares two property values in the manner specified by the property description. Returns two display strings that describe how the two properties compare.


## -parameters




### -param propvar1 [in]

Type: <b>REFPROPVARIANT</b>

A reference to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that contains the type and value of the first property.


### -param propvar2 [in]

Type: <b>REFPROPVARIANT</b>

A reference to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that contains the type and value of the second property.


### -param ppszDesc1 [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to the description string that compares the first property with the second property. The string is null-terminated.


### -param ppszDesc2 [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to the description string that compares the second property with the first property. The string is null-terminated.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is influenced by the <i>relativeDescriptionType</i> attribute of the <a href="https://msdn.microsoft.com/en-us/library/Bb773865(v=VS.85).aspx">displayInfo</a> element in the property's .propdesc file.

It is the responsibility of the calling application to release <i>ppszDesc1</i> and <i>ppszDesc2</i> through <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> when they are no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 


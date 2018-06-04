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

# PSPropertyBag_ReadUnknown function


## -description


Reads a given property of an unknown data value in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a>*</b>

A pointer to an <a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a> object, that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated property name string.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>. This interface IID should be <a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a> or an interface derived from <b>IPropertyBag</b>.


### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




<a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a> and <a href="_inet_IPersistPropertyBag_Interface">IPersistPropertyBag</a> optimize Save As Text functionality. <b>IPropertyBag</b> and <a href="_inet_IPropertyBag2_Interface">IPropertyBag2</a> provide an object with a property bag in which the object can save its properties persistently. <b>IPropertyBag2</b> allows the object to obtain type information for each property: <a href="_inet_IPropertyBag2_Read_Method">IPropertyBag2::Read</a> causes one or more properties to be read from the property bag, and <a href="_inet_IPropertyBag2_Write_Method">IPropertyBag2::Write</a> causes one or more properties to be saved into the property bag.




## -see-also




<a href="shell.PSPropertyBag_WriteUnknown">PSPropertyBag_WriteUnknown</a>
 

 


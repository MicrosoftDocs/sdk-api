---
UID: NF:propsys.PSPropertyBag_ReadUnknown
title: PSPropertyBag_ReadUnknown function
author: windows-sdk-content
description: Reads a given property of an unknown data value in a property bag.
old-location: properties\PSPropertyBag_ReadUnknown.htm
old-project: properties
ms.assetid: 87921F52-308F-4ed7-8390-A3C0217ACEFD
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PSPropertyBag_ReadUnknown, PSPropertyBag_ReadUnknown function [Windows Properties], properties.PSPropertyBag_ReadUnknown, propsys/PSPropertyBag_ReadUnknown, shell.PSPropertyBag_ReadUnknown, shell_PSPropertyBag_ReadUnknown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSPropertyBag_ReadUnknown
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
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
 

 


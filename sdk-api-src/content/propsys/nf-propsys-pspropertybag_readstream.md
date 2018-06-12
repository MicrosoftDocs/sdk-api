---
UID: NF:propsys.PSPropertyBag_ReadStream
title: PSPropertyBag_ReadStream function
author: windows-sdk-content
description: Reads the data stream stored in a given property contained in a specified property bag.
old-location: properties\PSPropertyBag_ReadStream.htm
old-project: properties
ms.assetid: 3D1D8B3E-DD16-4b34-918C-C8478EBF0930
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PSPropertyBag_ReadStream, PSPropertyBag_ReadStream function [Windows Properties], properties.PSPropertyBag_ReadStream, propsys/PSPropertyBag_ReadStream, shell.PSPropertyBag_ReadStream, shell_PSPropertyBag_ReadStream
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
 - PSPropertyBag_ReadStream
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PSPropertyBag_ReadStream function


## -description


Reads the data stream stored in a given property contained in a specified property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a>*</b>

A pointer to an <a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a> object, that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated property name string.


### -param value [out]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>**</b>

The address of a pointer that, when this function returns successfully, receives the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> object.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The caller of the <a href="shell.PSPropertyBag_ReadStream">PSPropertyBag_ReadStream</a> function needs to call a <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> object returned by this function.



<a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a> and <a href="_inet_IPersistPropertyBag_Interface">IPersistPropertyBag</a> optimize Save As Text functionality. <b>IPropertyBag</b> and <a href="_inet_IPropertyBag2_Interface">IPropertyBag2</a> provide an object with a property bag in which the object can save its properties persistently. <b>IPropertyBag2</b> allows the object to obtain type information for each property: <a href="_inet_IPropertyBag2_Read_Method">IPropertyBag2::Read</a> causes one or more properties to be read from the property bag, and <a href="_inet_IPropertyBag2_Write_Method">IPropertyBag2::Write</a> causes one or more properties to be saved into the property bag.




## -see-also




<a href="shell.PSPropertyBag_WriteStream">PSPropertyBag_WriteStream</a>
 

 


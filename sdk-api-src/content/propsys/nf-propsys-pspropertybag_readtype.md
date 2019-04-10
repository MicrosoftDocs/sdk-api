---
UID: NF:propsys.PSPropertyBag_ReadType
title: PSPropertyBag_ReadType function (propsys.h)
author: windows-sdk-content
description: Reads the type of data value of a property that is stored in a property bag.
old-location: properties\PSPropertyBag_ReadType.htm
tech.root: properties
ms.assetid: 826038F7-FD93-474e-BCA7-910E214F3E01
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_ReadType, PSPropertyBag_ReadType function [Windows Properties], properties.PSPropertyBag_ReadType, propsys/PSPropertyBag_ReadType, shell.PSPropertyBag_ReadType, shell_PSPropertyBag_ReadType
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
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSPropertyBag_ReadType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PSPropertyBag_ReadType function


## -description


Reads the type of data value of a property that is stored in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a> object, that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated property name string.


### -param var [out]

Type: <b>VARIANT*</b>

Returns on successful function completion a pointer to a <b>VARIANT</b> data type that contains the property value.


### -param type [out]

Type: <b>VARTYPE*</b>

If <i>type</i> is VT_EMPTY, this function reads the <b>VARIANT</b> of the property in the IPropertyBag   <i>propBag</i> parameter. If <i>type</i> is not VT_EMPTY and not the same as the <b>VARIANT</b> read, then this function attempts to convert the <b>VARIANT</b> read to the <b>VARTYPE</b> defined by <i>type</i> parameter before returning.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




<a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a> and <a href="https://msdn.microsoft.com/library/Aa768205(v=VS.85).aspx">IPersistPropertyBag</a> optimize Save As Text functionality. <b>IPropertyBag</b> and <a href="https://msdn.microsoft.com/library/Aa768192(v=VS.85).aspx">IPropertyBag2</a> provide an object with a property bag in which the object can save its properties persistently. <b>IPropertyBag2</b> allows the object to obtain type information for each property: <a href="https://msdn.microsoft.com/library/Aa768194(v=VS.85).aspx">IPropertyBag2::Read</a> causes one or more properties to be read from the property bag, and <a href="https://msdn.microsoft.com/library/Aa768195(v=VS.85).aspx">IPropertyBag2::Write</a> causes one or more properties to be saved into the property bag.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee845049(v=VS.85).aspx">PSPropertyBag_Delete</a>
 

 


---
UID: NF:propsys.PSPropertyBag_ReadUnknown
title: PSPropertyBag_ReadUnknown function
author: windows-sdk-content
description: Reads a given property of an unknown data value in a property bag.
old-location: properties\PSPropertyBag_ReadUnknown.htm
tech.root: properties
ms.assetid: 87921F52-308F-4ed7-8390-A3C0217ACEFD
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PSPropertyBag_ReadUnknown, PSPropertyBag_ReadUnknown function [Windows Properties], properties.PSPropertyBag_ReadUnknown, propsys/PSPropertyBag_ReadUnknown, shell.PSPropertyBag_ReadUnknown, shell_PSPropertyBag_ReadUnknown
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
 - PSPropertyBag_ReadUnknown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PSPropertyBag_ReadUnknown function


## -description


Reads a given property of an unknown data value in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a> object, that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated property name string.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>. This interface IID should be <a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a> or an interface derived from <b>IPropertyBag</b>.


### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




<a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a> and <a href="https://msdn.microsoft.com/library/Aa768205(v=VS.85).aspx">IPersistPropertyBag</a> optimize Save As Text functionality. <b>IPropertyBag</b> and <a href="https://msdn.microsoft.com/library/Aa768192(v=VS.85).aspx">IPropertyBag2</a> provide an object with a property bag in which the object can save its properties persistently. <b>IPropertyBag2</b> allows the object to obtain type information for each property: <a href="https://msdn.microsoft.com/library/Aa768194(v=VS.85).aspx">IPropertyBag2::Read</a> causes one or more properties to be read from the property bag, and <a href="https://msdn.microsoft.com/library/Aa768195(v=VS.85).aspx">IPropertyBag2::Write</a> causes one or more properties to be saved into the property bag.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee845081(v=VS.85).aspx">PSPropertyBag_WriteUnknown</a>
 

 


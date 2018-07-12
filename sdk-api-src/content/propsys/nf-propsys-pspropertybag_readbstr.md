---
UID: NF:propsys.PSPropertyBag_ReadBSTR
title: PSPropertyBag_ReadBSTR function
author: windows-sdk-content
description: Reads a BSTR data value from a property in a property bag.
old-location: properties\PSPropertyBag_ReadBSTR.htm
old-project: properties
ms.assetid: 14F21A4D-4867-4c4d-9BD8-C733B1C50266
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: PSPropertyBag_ReadBSTR, PSPropertyBag_ReadBSTR function [Windows Properties], properties.PSPropertyBag_ReadBSTR, propsys/PSPropertyBag_ReadBSTR, shell.PSPropertyBag_ReadBSTR, shell_PSPropertyBag_ReadBSTR
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
 - PSPropertyBag_ReadBSTR
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# PSPropertyBag_ReadBSTR function


## -description


Reads a <b>BSTR</b> data value from a property in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a>*</b>

A pointer to an <a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.


### -param value [out]

Type: <b><a href="https://msdn.microsoft.com/library/ms221069(v=VS.85).aspx">BSTR</a>*</b>

When this function returns, contains a pointer to a <b>BSTR</b> property value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag.  Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="https://msdn.microsoft.com/library/Ee845068(v=VS.85).aspx">PSPropertyBag_WriteBSTR</a>
 

 


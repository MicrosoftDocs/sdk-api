---
UID: NF:propsys.PSPropertyBag_WriteBOOL
title: PSPropertyBag_WriteBOOL function
author: windows-sdk-content
description: Sets the BOOL value of a property in a property bag.
old-location: properties\PSPropertyBag_WriteBOOL.htm
tech.root: properties
ms.assetid: 3703A7C4-CFDC-4453-AA8F-6A5D6B7D3E66
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PSPropertyBag_WriteBOOL, PSPropertyBag_WriteBOOL function [Windows Properties], properties.PSPropertyBag_WriteBOOL, propsys/PSPropertyBag_WriteBOOL, shell.PSPropertyBag_WriteBOOL, shell_PSPropertyBag_WriteBOOL
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - PSPropertyBag_WriteBOOL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- PSPropertyBag_WriteBOOL
: 
---

# PSPropertyBag_WriteBOOL function


## -description


Sets the <b>BOOL</b> value of a property in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.


### -param value [in]

Type: <b>BOOL</b>

The <b>BOOL</b> value to which the named property should be set.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee845050(v=VS.85).aspx">PSPropertyBag_ReadBOOL</a>
 

 


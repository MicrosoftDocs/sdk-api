---
UID: NF:propsys.PSPropertyBag_WriteLONG
title: PSPropertyBag_WriteLONG function (propsys.h)
author: windows-sdk-content
description: Sets the LONG value of a property in a property bag.
old-location: properties\PSPropertyBag_WriteLONG.htm
tech.root: properties
ms.assetid: A623D097-FEF8-4864-A80A-C6EF824EC245
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_WriteLONG, PSPropertyBag_WriteLONG function [Windows Properties], properties.PSPropertyBag_WriteLONG, propsys/PSPropertyBag_WriteLONG, shell.PSPropertyBag_WriteLONG, shell_PSPropertyBag_WriteLONG
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
 - PSPropertyBag_WriteLONG
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PSPropertyBag_WriteLONG function


## -description


Sets the <b>LONG</b> value of a property in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.


### -param value [in]

Type: <b>LONG</b>

The <b>LONG</b> value to which the property should be set.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee845055(v=VS.85).aspx">PSPropertyBag_ReadLONG</a>
 

 


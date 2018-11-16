---
UID: NF:propsys.PSPropertyBag_ReadULONGLONG
title: PSPropertyBag_ReadULONGLONG function
author: windows-sdk-content
description: Reads a ULONGLONG data value from a property in a property bag.
old-location: properties\PSPropertyBag_ReadULONGLONG.htm
tech.root: properties
ms.assetid: 6DB59A95-D571-452b-8974-76B4CC3FA36F
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PSPropertyBag_ReadULONGLONG, PSPropertyBag_ReadULONGLONG function [Windows Properties], properties.PSPropertyBag_ReadULONGLONG, propsys/PSPropertyBag_ReadULONGLONG, shell.PSPropertyBag_ReadULONGLONG, shell_PSPropertyBag_ReadULONGLONG
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
 - PSPropertyBag_ReadULONGLONG
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- PSPropertyBag_ReadULONGLONG
: 
---

# PSPropertyBag_ReadULONGLONG function


## -description


Reads a <b>ULONGLONG</b> data value from a property in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.


### -param value [out]

Type: <b>ULONGLONG</b>

When this function returns, contains a pointer to a <b>ULONGLONG</b> property value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee845080(v=VS.85).aspx">PSPropertyBag_WriteULONGLONG</a>
 

 


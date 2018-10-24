---
UID: NF:propsys.PSPropertyBag_WriteULONGLONG
title: PSPropertyBag_WriteULONGLONG function
author: windows-sdk-content
description: Sets the ULONGLONG value of a property in a property bag.
old-location: properties\PSPropertyBag_WriteULONGLONG.htm
tech.root: properties
ms.assetid: 37854C80-00B9-465c-88D9-619695D418CD
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: PSPropertyBag_WriteULONGLONG, PSPropertyBag_WriteULONGLONG function [Windows Properties], properties.PSPropertyBag_WriteULONGLONG, propsys/PSPropertyBag_WriteULONGLONG, shell.PSPropertyBag_WriteULONGLONG, shell_PSPropertyBag_WriteULONGLONG
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
 - PSPropertyBag_WriteULONGLONG
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PSPropertyBag_WriteULONGLONG function


## -description


Sets the <b>ULONGLONG</b> value of a property in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a>*</b>

A pointer to an <a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.


### -param value [in]

Type: <b>ULONGLONG</b>

An <b>ULONGLONG</b> value to which the property should be set.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="shell.PSPropertyBag_ReadULONGLONG">PSPropertyBag_ReadULONGLONG</a>
 

 


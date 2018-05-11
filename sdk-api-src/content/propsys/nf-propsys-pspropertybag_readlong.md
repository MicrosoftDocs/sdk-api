---
UID: NF:propsys.PSPropertyBag_ReadLONG
title: PSPropertyBag_ReadLONG function
author: windows-driver-content
description: Reads a LONG data value from a property in a property bag.
old-location: properties\PSPropertyBag_ReadLONG.htm
old-project: properties
ms.assetid: A39E1F7C-A4FB-47da-A05E-39F6176F2878
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PSPropertyBag_ReadLONG, PSPropertyBag_ReadLONG function [Windows Properties], properties.PSPropertyBag_ReadLONG, propsys/PSPropertyBag_ReadLONG, shell.PSPropertyBag_ReadLONG, shell_PSPropertyBag_ReadLONG
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: propsys.h
req.include-header: Propsys.idl
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
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	PSPropertyBag_ReadLONG
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PSPropertyBag_ReadLONG function


## -description


Reads a <b>LONG</b> data value from a property in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a>*</b>

A pointer to an <a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.


### -param value [out]

Type: <b>LONG*</b>

When this function returns, contains a pointer to a <b>LONG</b> property value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the property bag does not already contain the specified property, the call still succeeds.

The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="shell.PSPropertyBag_WriteLONG">PSPropertyBag_WriteLONG</a>
 

 


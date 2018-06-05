---
UID: NF:propsys.PSPropertyBag_ReadInt
title: PSPropertyBag_ReadInt function
author: windows-sdk-content
description: Reads an int data value from a property in a property bag.
old-location: properties\PSPropertyBag_ReadInt.htm
old-project: properties
ms.assetid: 9CEC97E6-C88F-4182-876C-D77EA14915DA
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PSPropertyBag_ReadInt, PSPropertyBag_ReadInt function [Windows Properties], properties.PSPropertyBag_ReadInt, propsys/PSPropertyBag_ReadInt, shell.PSPropertyBag_ReadInt, shell_PSPropertyBag_ReadInt
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	PSPropertyBag_ReadInt
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PSPropertyBag_ReadInt function


## -description


Reads an <b>int</b> data value from a property in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a>*</b>

A pointer to an <a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.


### -param value [out]

Type: <b>int*</b>

When this function returns, contains a pointer to an <b>int</b> property value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the property bag does not already contain the specified property, the call still succeeds.

The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="shell.PSPropertyBag_WriteInt">PSPropertyBag_WriteInt</a>
 

 


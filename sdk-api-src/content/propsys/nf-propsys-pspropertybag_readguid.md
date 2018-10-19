---
UID: NF:propsys.PSPropertyBag_ReadGUID
title: PSPropertyBag_ReadGUID function
author: windows-sdk-content
description: Reads the GUID data value from a property in a property bag.
old-location: properties\PSPropertyBag_ReadGUID.htm
tech.root: properties
ms.assetid: BCC6E830-CF05-42c1-874F-CCC97E58A4BC
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: PSPropertyBag_ReadGUID, PSPropertyBag_ReadGUID function [Windows Properties], properties.PSPropertyBag_ReadGUID, propsys/PSPropertyBag_ReadGUID, shell.PSPropertyBag_ReadGUID, shell_PSPropertyBag_ReadGUID
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
 - PSPropertyBag_ReadGUID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PSPropertyBag_ReadGUID function


## -description


Reads the GUID data value from a property in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a>*</b>

A pointer to an <a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.


### -param value [out]

Type: <b>GUID*</b>

When this function returns, contains a pointer to a GUID property value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="shell.PSPropertyBag_WriteGUID">PSPropertyBag_WriteGUID</a>
 

 


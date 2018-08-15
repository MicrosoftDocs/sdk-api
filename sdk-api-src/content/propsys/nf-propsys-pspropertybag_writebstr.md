---
UID: NF:propsys.PSPropertyBag_WriteBSTR
title: PSPropertyBag_WriteBSTR function
author: windows-sdk-content
description: Sets the BSTR value of a property in a property bag.
old-location: properties\PSPropertyBag_WriteBSTR.htm
old-project: properties
ms.assetid: 9C2DBD1F-6760-4812-A33E-9A71C5A421A9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PSPropertyBag_WriteBSTR, PSPropertyBag_WriteBSTR function [Windows Properties], properties.PSPropertyBag_WriteBSTR, propsys/PSPropertyBag_WriteBSTR, shell.PSPropertyBag_WriteBSTR, shell_PSPropertyBag_WriteBSTR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propsys.h
req.include-header: 
req.redist: 
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
 - PSPropertyBag_WriteBSTR
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# PSPropertyBag_WriteBSTR function


## -description


Sets the <b>BSTR</b> value of a property in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a>*</b>

A pointer to an <a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.


### -param value [in]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a></b>

The <b>BSTR</b> value to which the named property should be set.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="shell.PSPropertyBag_ReadBSTR">PSPropertyBag_ReadBSTR</a>
 

 


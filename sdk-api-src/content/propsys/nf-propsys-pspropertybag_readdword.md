---
UID: NF:propsys.PSPropertyBag_ReadDWORD
title: PSPropertyBag_ReadDWORD function
author: windows-sdk-content
description: Reads a DWORD data value from property in a property bag.
old-location: properties\PSPropertyBag_ReadDWORD.htm
old-project: properties
ms.assetid: 31977E3F-FA2F-4c2d-8A95-6BF937EDC45C
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: PSPropertyBag_ReadDWORD, PSPropertyBag_ReadDWORD function [Windows Properties], properties.PSPropertyBag_ReadDWORD, propsys/PSPropertyBag_ReadDWORD, shell.PSPropertyBag_ReadDWORD, shell_PSPropertyBag_ReadDWORD
ms.prod: windows
ms.technology: windows-sdk
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
 - PSPropertyBag_ReadDWORD
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# PSPropertyBag_ReadDWORD function


## -description


Reads a <b>DWORD</b> data value from property in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a>*</b>

A pointer to an <a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated property name string.


### -param value [out]

Type: <b>DWORD*</b>

When this function returns, contains a pointer to a <b>DWORD</b> property value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="https://msdn.microsoft.com/library/Ee845069(v=VS.85).aspx">PSPropertyBag_WriteDWORD</a>
 

 


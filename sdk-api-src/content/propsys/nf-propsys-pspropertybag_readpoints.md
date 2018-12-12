---
UID: NF:propsys.PSPropertyBag_ReadPOINTS
title: PSPropertyBag_ReadPOINTS function
author: windows-sdk-content
description: Retrieves the property coordinates stored in a POINTS structure of a specified property bag.
old-location: properties\PSPropertyBag_ReadPOINTS.htm
tech.root: properties
ms.assetid: 60ED145A-7712-43b7-A2AD-C366DD32E19E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PSPropertyBag_ReadPOINTS, PSPropertyBag_ReadPOINTS function [Windows Properties], properties.PSPropertyBag_ReadPOINTS, propsys/PSPropertyBag_ReadPOINTS, shell.PSPropertyBag_ReadPOINTS, shell_PSPropertyBag_ReadPOINTS
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
 - PSPropertyBag_ReadPOINTS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PSPropertyBag_ReadPOINTS function


## -description


Retrieves the property coordinates stored in a <a href="https://msdn.microsoft.com/d36bc846-c538-4a37-bb5d-c75d41a3c7cc">POINTS</a> structure of a specified property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a>*</b>

A pointer to an <a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.


### -param value [out]

Type: <b><a href="https://msdn.microsoft.com/d36bc846-c538-4a37-bb5d-c75d41a3c7cc">POINTS</a>*</b>

When this function returns successfully, contains a pointer to a <a href="https://msdn.microsoft.com/d36bc846-c538-4a37-bb5d-c75d41a3c7cc">POINTS</a> structure that contains the property coordinates.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="shell.PSPropertyBag_WritePOINTS">PSPropertyBag_WritePOINTS</a>
 

 


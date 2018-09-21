---
UID: NF:propsys.PSPropertyBag_WritePOINTS
title: PSPropertyBag_WritePOINTS function
author: windows-sdk-content
description: Stores the property coordinates in aPOINTS structure of a specified property bag.
old-location: properties\PSPropertyBag_WritePOINTS.htm
tech.root: properties
ms.assetid: B1E3E061-042A-4ba0-98F2-EA8A022882CC
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: PSPropertyBag_WritePOINTS, PSPropertyBag_WritePOINTS function [Windows Properties], properties.PSPropertyBag_WritePOINTS, propsys/PSPropertyBag_WritePOINTS, shell.PSPropertyBag_WritePOINTS, shell_PSPropertyBag_WritePOINTS
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
 - PSPropertyBag_WritePOINTS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PSPropertyBag_WritePOINTS function


## -description


 Stores the property coordinates in a<a href="https://msdn.microsoft.com/d36bc846-c538-4a37-bb5d-c75d41a3c7cc">POINTS</a> structure of a specified property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/library/Aa768196(v=VS.85).aspx">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.


### -param value [in]

Type: <b>const <a href="https://msdn.microsoft.com/d36bc846-c538-4a37-bb5d-c75d41a3c7cc">POINTS</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/d36bc846-c538-4a37-bb5d-c75d41a3c7cc">POINTS</a> structure that specifies the coordinates to store in the property.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee845057(v=VS.85).aspx">PSPropertyBag_ReadPOINTS</a>
 

 


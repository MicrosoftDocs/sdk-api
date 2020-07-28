---
UID: NF:propsys.PSPropertyBag_ReadPOINTS
title: PSPropertyBag_ReadPOINTS function (propsys.h)
description: Retrieves the property coordinates stored in a POINTS structure of a specified property bag.
helpviewer_keywords: ["PSPropertyBag_ReadPOINTS","PSPropertyBag_ReadPOINTS function [Windows Properties]","properties.PSPropertyBag_ReadPOINTS","propsys/PSPropertyBag_ReadPOINTS","shell.PSPropertyBag_ReadPOINTS","shell_PSPropertyBag_ReadPOINTS"]
old-location: properties\PSPropertyBag_ReadPOINTS.htm
tech.root: properties
ms.assetid: 60ED145A-7712-43b7-A2AD-C366DD32E19E
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_ReadPOINTS, PSPropertyBag_ReadPOINTS function [Windows Properties], properties.PSPropertyBag_ReadPOINTS, propsys/PSPropertyBag_ReadPOINTS, shell.PSPropertyBag_ReadPOINTS, shell_PSPropertyBag_ReadPOINTS
f1_keywords:
- propsys/PSPropertyBag_ReadPOINTS
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PSPropertyBag_ReadPOINTS function


## -description


Retrieves the property coordinates stored in a <a href="https://docs.microsoft.com/previous-versions/dd162808(v=vs.85)">POINTS</a> structure of a specified property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.


### -param value [out]

Type: <b><a href="https://docs.microsoft.com/previous-versions/dd162808(v=vs.85)">POINTS</a>*</b>

When this function returns successfully, contains a pointer to a <a href="https://docs.microsoft.com/previous-versions/dd162808(v=vs.85)">POINTS</a> structure that contains the property coordinates.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-pspropertybag_writepoints">PSPropertyBag_WritePOINTS</a>
 

 


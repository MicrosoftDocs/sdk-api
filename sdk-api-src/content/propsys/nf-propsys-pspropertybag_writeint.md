---
UID: NF:propsys.PSPropertyBag_WriteInt
title: PSPropertyBag_WriteInt function (propsys.h)
description: Sets the int value of a property in a property bag.helpviewer_keywords: ["PSPropertyBag_WriteInt","PSPropertyBag_WriteInt function [Windows Properties]","properties.PSPropertyBag_WriteInt","propsys/PSPropertyBag_WriteInt","shell.PSPropertyBag_WriteInt","shell_PSPropertyBag_WriteInt"]
old-location: properties\PSPropertyBag_WriteInt.htm
tech.root: properties
ms.assetid: 1FCC59B1-5084-4981-8F1D-A5860744F221
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_WriteInt, PSPropertyBag_WriteInt function [Windows Properties], properties.PSPropertyBag_WriteInt, propsys/PSPropertyBag_WriteInt, shell.PSPropertyBag_WriteInt, shell_PSPropertyBag_WriteInt
f1_keywords:
- propsys/PSPropertyBag_WriteInt
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
- PSPropertyBag_WriteInt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PSPropertyBag_WriteInt function


## -description


Sets the <b>int</b> value of a property in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.


### -param value [in]

Type: <b>int</b>

The <b>int</b> value to which the property should be set.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-pspropertybag_readint">PSPropertyBag_ReadInt</a>
 

 


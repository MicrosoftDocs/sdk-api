---
UID: NF:propsys.PSPropertyBag_ReadDWORD
title: PSPropertyBag_ReadDWORD function (propsys.h)
description: Reads a DWORD data value from property in a property bag.
helpviewer_keywords: ["PSPropertyBag_ReadDWORD","PSPropertyBag_ReadDWORD function [Windows Properties]","properties.PSPropertyBag_ReadDWORD","propsys/PSPropertyBag_ReadDWORD","shell.PSPropertyBag_ReadDWORD","shell_PSPropertyBag_ReadDWORD"]
old-location: properties\PSPropertyBag_ReadDWORD.htm
tech.root: properties
ms.assetid: 31977E3F-FA2F-4c2d-8A95-6BF937EDC45C
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_ReadDWORD, PSPropertyBag_ReadDWORD function [Windows Properties], properties.PSPropertyBag_ReadDWORD, propsys/PSPropertyBag_ReadDWORD, shell.PSPropertyBag_ReadDWORD, shell_PSPropertyBag_ReadDWORD
f1_keywords:
- propsys/PSPropertyBag_ReadDWORD
dev_langs:
- c++
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
- PSPropertyBag_ReadDWORD
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PSPropertyBag_ReadDWORD function


## -description


Reads a <b>DWORD</b> data value from property in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a> object that represents the property bag in which the property is stored.


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




<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-pspropertybag_writedword">PSPropertyBag_WriteDWORD</a>
 

 


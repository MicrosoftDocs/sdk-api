---
UID: NF:propsys.PSPropertyBag_WriteGUID
title: PSPropertyBag_WriteGUID function (propsys.h)
description: Sets the GUID value of a property in a property bag.
helpviewer_keywords: ["PSPropertyBag_WriteGUID","PSPropertyBag_WriteGUID function [Windows Properties]","properties.PSPropertyBag_WriteGUID","propsys/PSPropertyBag_WriteGUID","shell.PSPropertyBag_WriteGUID","shell_PSPropertyBag_WriteGUID"]
old-location: properties\PSPropertyBag_WriteGUID.htm
tech.root: properties
ms.assetid: F50CF010-3A4E-4723-BA9F-CE1B48CA4AA4
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_WriteGUID, PSPropertyBag_WriteGUID function [Windows Properties], properties.PSPropertyBag_WriteGUID, propsys/PSPropertyBag_WriteGUID, shell.PSPropertyBag_WriteGUID, shell_PSPropertyBag_WriteGUID
f1_keywords:
- propsys/PSPropertyBag_WriteGUID
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
- PSPropertyBag_WriteGUID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PSPropertyBag_WriteGUID function


## -description


Sets the GUID value of a property in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.


### -param value [in]

Type: <b>const GUID*</b>

A pointer to a GUID value to which the named property should be set.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag.  Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-pspropertybag_readguid">PSPropertyBag_ReadGUID</a>
 

 


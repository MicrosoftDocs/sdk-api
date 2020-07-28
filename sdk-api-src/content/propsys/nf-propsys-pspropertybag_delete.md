---
UID: NF:propsys.PSPropertyBag_Delete
title: PSPropertyBag_Delete function (propsys.h)
description: Deletes a property from a property bag.
helpviewer_keywords: ["PSPropertyBag_Delete","PSPropertyBag_Delete function [Windows Properties]","properties.PSPropertyBag_Delete","propsys/PSPropertyBag_Delete","shell.PSPropertyBag_Delete","shell_PSPropertyBag_Delete"]
old-location: properties\PSPropertyBag_Delete.htm
tech.root: properties
ms.assetid: 53ED1C87-5141-4925-B70E-C0304817A871
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_Delete, PSPropertyBag_Delete function [Windows Properties], properties.PSPropertyBag_Delete, propsys/PSPropertyBag_Delete, shell.PSPropertyBag_Delete, shell_PSPropertyBag_Delete
f1_keywords:
- propsys/PSPropertyBag_Delete
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
- PSPropertyBag_Delete
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PSPropertyBag_Delete function


## -description


Deletes a property from a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-pspropertybag_readtype">PSPropertyBag_ReadType</a>
 

 


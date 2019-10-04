---
UID: NF:propsys.PSPropertyBag_ReadLONG
title: PSPropertyBag_ReadLONG function (propsys.h)
author: windows-sdk-content
description: Reads a LONG data value from a property in a property bag.
old-location: properties\PSPropertyBag_ReadLONG.htm
tech.root: properties
ms.assetid: A39E1F7C-A4FB-47da-A05E-39F6176F2878
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_ReadLONG, PSPropertyBag_ReadLONG function [Windows Properties], properties.PSPropertyBag_ReadLONG, propsys/PSPropertyBag_ReadLONG, shell.PSPropertyBag_ReadLONG, shell_PSPropertyBag_ReadLONG
ms.topic: function
f1_keywords: 
 - "propsys/PSPropertyBag_ReadLONG"
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
 - PSPropertyBag_ReadLONG
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PSPropertyBag_ReadLONG function


## -description


Reads a <b>LONG</b> data value from a property in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.


### -param value [out]

Type: <b>LONG*</b>

When this function returns, contains a pointer to a <b>LONG</b> property value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the property bag does not already contain the specified property, the call still succeeds.

The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-pspropertybag_writelong">PSPropertyBag_WriteLONG</a>
 

 


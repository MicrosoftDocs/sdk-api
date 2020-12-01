---
UID: NF:propsys.PSEnumeratePropertyDescriptions
title: PSEnumeratePropertyDescriptions function (propsys.h)
description: A wrapper API that calls the schema subsystem's IPropertySystem::EnumeratePropertyDescriptions.
helpviewer_keywords: ["PSEnumeratePropertyDescriptions","PSEnumeratePropertyDescriptions function [Windows Properties]","properties.PSEnumeratePropertyDescriptions","propsys/PSEnumeratePropertyDescriptions","shell.PSEnumeratePropertyDescriptions","shell_PSEnumeratePropertyDescriptions"]
old-location: properties\PSEnumeratePropertyDescriptions.htm
tech.root: properties
ms.assetid: 687d5a32-3a2e-4b9b-b06c-ca06a6cd1595
ms.date: 12/05/2018
ms.keywords: PSEnumeratePropertyDescriptions, PSEnumeratePropertyDescriptions function [Windows Properties], properties.PSEnumeratePropertyDescriptions, propsys/PSEnumeratePropertyDescriptions, shell.PSEnumeratePropertyDescriptions, shell_PSEnumeratePropertyDescriptions
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - PSEnumeratePropertyDescriptions
 - propsys/PSEnumeratePropertyDescriptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSEnumeratePropertyDescriptions
---

# PSEnumeratePropertyDescriptions function


## -description

A wrapper API that calls the schema subsystem's <a href="/windows/desktop/api/propsys/nf-propsys-ipropertysystem-enumeratepropertydescriptions">IPropertySystem::EnumeratePropertyDescriptions</a>. This function retrieves an instance of the subsystem object that implements <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a>, to obtain either the entire list or a partial list of property descriptions in the system.

## -parameters

### -param filterOn [in]

Type: <b><a href="/windows/desktop/api/propsys/ne-propsys-propdesc_enumfilter">PROPDESC_ENUMFILTER</a></b>

The list to return. <a href="/windows/desktop/api/propsys/ne-propsys-propdesc_enumfilter">PROPDESC_ENUMFILTER</a> shows the valid values for this method.

### -param riid [in]

Type: <b>REFIID</b>

Reference to the  interface ID of the requested interface.

### -param ppv [out]

Type: <b>void**</b>

The address of an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a> interface pointer.

## -returns

Type: <b>PSSTDAPI</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Indicates an interface is obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that <i>ppv</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

We recommend that you use the IID_PPV_ARGS macro, defined in objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, eliminating the possibility of a coding error.
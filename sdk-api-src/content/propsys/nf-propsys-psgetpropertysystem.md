---
UID: NF:propsys.PSGetPropertySystem
title: PSGetPropertySystem function (propsys.h)
description: Gets an instance of the subsystem object that implements IPropertySystem.
helpviewer_keywords: ["PSGetPropertySystem","PSGetPropertySystem function [Windows Properties]","properties.PSGetPropertySystem","propsys/PSGetPropertySystem","shell.PSGetPropertySystem","shell_PSGetPropertySystem"]
old-location: properties\PSGetPropertySystem.htm
tech.root: properties
ms.assetid: ddbf7cea-b22f-4cf9-8b5f-804640086466
ms.date: 12/05/2018
ms.keywords: PSGetPropertySystem, PSGetPropertySystem function [Windows Properties], properties.PSGetPropertySystem, propsys/PSGetPropertySystem, shell.PSGetPropertySystem, shell_PSGetPropertySystem
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
 - PSGetPropertySystem
 - propsys/PSGetPropertySystem
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
 - PSGetPropertySystem
---

# PSGetPropertySystem function


## -description

Gets an instance of the subsystem object that implements <a href="/windows/desktop/api/propsys/nn-propsys-ipropertysystem">IPropertySystem</a>.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

Reference to the IID of the requested interface.

### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/propsys/nn-propsys-ipropertysystem">IPropertySystem</a>.

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
The interface was obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppv</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

You must initialize Component Object Model (COM) with <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> prior to calling <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertysystem">PSGetPropertySystem</a>.  COM must remain initialized for the lifetime of this object. The property system object aggregates the free-threaded marshaller and is thread-safe.

We recommend that you use the IID_PPV_ARGS macro defined in Objbase.h to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertysystem">PSGetPropertySystem</a>.


```cpp
IPropertySystem *pSystem;

HRESULT hr = PSGetPropertySystem(IID_PPV_ARGS(&pSystem));

if (SUCCEEDED(hr))
{
    // pSystem is now valid.
 
    pSystem->Release();
}
```
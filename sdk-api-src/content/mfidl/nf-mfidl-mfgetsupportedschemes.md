---
UID: NF:mfidl.MFGetSupportedSchemes
title: MFGetSupportedSchemes function (mfidl.h)
description: Retrieves the URL schemes that are registered for the source resolver.
helpviewer_keywords: ["MFGetSupportedSchemes","MFGetSupportedSchemes function [Media Foundation]","b40315fc-7e2b-4573-a98f-840b6ce31dd3","mf.mfgetsupportedschemes","mfidl/MFGetSupportedSchemes"]
old-location: mf\mfgetsupportedschemes.htm
tech.root: mf
ms.assetid: b40315fc-7e2b-4573-a98f-840b6ce31dd3
ms.date: 12/05/2018
ms.keywords: MFGetSupportedSchemes, MFGetSupportedSchemes function [Media Foundation], b40315fc-7e2b-4573-a98f-840b6ce31dd3, mf.mfgetsupportedschemes, mfidl/MFGetSupportedSchemes
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFGetSupportedSchemes
 - mfidl/MFGetSupportedSchemes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFGetSupportedSchemes
---

# MFGetSupportedSchemes function


## -description

Retrieves the URL schemes that are registered for the source resolver.

## -parameters

### -param pPropVarSchemeArray [out]

Pointer to a <b>PROPVARIANT</b> that receives the URL schemes. Before calling this method, call <b>PropVariantInit</b> to initialize the <b>PROPVARIANT</b>. If the method succeeds, the <b>PROPVARIANT</b> contains an array of wide-character strings. The <b>PROPVARIANT</b> data type is VT_VECTOR | VT_LPWSTR. The caller must release the <b>PROPVARIANT</b> by calling <b>PropVariantClear</b>.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
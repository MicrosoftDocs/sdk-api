---
UID: NF:wmsdkidl.WMCreateEditor
title: WMCreateEditor function (wmsdkidl.h)
description: The WMCreateEditor function creates a metadata editor object.
helpviewer_keywords: ["WMCreateEditor","WMCreateEditor function [windows Media Format]","wmformat.wmcreateeditor","wmsdkidl/WMCreateEditor"]
old-location: wmformat\wmcreateeditor.htm
tech.root: wmformat
ms.assetid: 3eed88d5-18e9-40b4-998d-af33ac5440b2
ms.date: 12/05/2018
ms.keywords: WMCreateEditor, WMCreateEditor function [windows Media Format], wmformat.wmcreateeditor, wmsdkidl/WMCreateEditor
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMCreateEditor
 - wmsdkidl/WMCreateEditor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wmvcore.dll
api_name:
 - WMCreateEditor
---

# WMCreateEditor function


## -description

The <b>WMCreateEditor</b> function creates a metadata editor object.

## -parameters

### -param ppEditor [out]

Pointer to a pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor">IWMMetadataEditor</a> interface of the newly created metadata editor object.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function is unable to allocate memory for the new object.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wmformat/functions">Functions</a>



<a href="/windows/desktop/wmformat/metadata-editor-object">Metadata Editor Object</a>
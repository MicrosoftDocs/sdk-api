---
UID: NF:mfidl.MFCreateTopoLoader
title: MFCreateTopoLoader function (mfidl.h)
description: Creates a new instance of the topology loader.
helpviewer_keywords: ["0c0173ef-9c29-465c-b725-ce38b220f94f","MFCreateTopoLoader","MFCreateTopoLoader function [Media Foundation]","mf.mfcreatetopoloader","mfidl/MFCreateTopoLoader"]
old-location: mf\mfcreatetopoloader.htm
tech.root: mf
ms.assetid: 0c0173ef-9c29-465c-b725-ce38b220f94f
ms.date: 12/05/2018
ms.keywords: 0c0173ef-9c29-465c-b725-ce38b220f94f, MFCreateTopoLoader, MFCreateTopoLoader function [Media Foundation], mf.mfcreatetopoloader, mfidl/MFCreateTopoLoader
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
 - MFCreateTopoLoader
 - mfidl/MFCreateTopoLoader
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
 - MFCreateTopoLoader
---

# MFCreateTopoLoader function


## -description

Creates a new instance of the topology loader.

## -parameters

### -param ppObj

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopoloader">IMFTopoLoader</a> interface of the topology loader. The caller must release the interface.

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
---
UID: NF:mfidl.MFCreateSystemTimeSource
title: MFCreateSystemTimeSource function (mfidl.h)
description: Creates a presentation time source that is based on the system time.
helpviewer_keywords: ["MFCreateSystemTimeSource","MFCreateSystemTimeSource function [Media Foundation]","f3e7b8d5-fd6c-4d87-86f6-1117ca58bc6f","mf.mfcreatesystemtimesource","mfidl/MFCreateSystemTimeSource"]
old-location: mf\mfcreatesystemtimesource.htm
tech.root: mf
ms.assetid: f3e7b8d5-fd6c-4d87-86f6-1117ca58bc6f
ms.date: 12/05/2018
ms.keywords: MFCreateSystemTimeSource, MFCreateSystemTimeSource function [Media Foundation], f3e7b8d5-fd6c-4d87-86f6-1117ca58bc6f, mf.mfcreatesystemtimesource, mfidl/MFCreateSystemTimeSource
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateSystemTimeSource
 - mfidl/MFCreateSystemTimeSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateSystemTimeSource
---

# MFCreateSystemTimeSource function


## -description

Creates a presentation time source that is based on the system time.

## -parameters

### -param ppSystemTimeSource

Receives a pointer to the object's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource">IMFPresentationTimeSource</a> interface. The caller must release the interface.

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
---
UID: NF:wmcontainer.MFCreateASFMediaSinkActivate
title: MFCreateASFMediaSinkActivate function (wmcontainer.h)
description: Creates an activation object that can be used to create the ASF media sink.
helpviewer_keywords: ["513d0a33-1504-4b88-9629-9e3e0dde3617","MFCreateASFMediaSinkActivate","MFCreateASFMediaSinkActivate function [Media Foundation]","mf.mfcreateasfmediasinkactivate","wmcontainer/MFCreateASFMediaSinkActivate"]
old-location: mf\mfcreateasfmediasinkactivate.htm
tech.root: mf
ms.assetid: 513d0a33-1504-4b88-9629-9e3e0dde3617
ms.date: 12/05/2018
ms.keywords: 513d0a33-1504-4b88-9629-9e3e0dde3617, MFCreateASFMediaSinkActivate, MFCreateASFMediaSinkActivate function [Media Foundation], mf.mfcreateasfmediasinkactivate, wmcontainer/MFCreateASFMediaSinkActivate
req.header: wmcontainer.h
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
 - MFCreateASFMediaSinkActivate
 - wmcontainer/MFCreateASFMediaSinkActivate
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
 - MFCreateASFMediaSinkActivate
---

# MFCreateASFMediaSinkActivate function


## -description

Creates an activation object that can be used to create the ASF media sink.

## -parameters

### -param pwszFileName

Null-terminated wide-character string that contains the output file name.

### -param pContentInfo

A pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a> interface of an initialized <a href="/windows/desktop/medfound/asf-file-structure">ASF Header Object</a> object. Use this interface to configure the ASF media sink.

### -param ppIActivate

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface. The caller must release the interface.

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

<a href="/windows/desktop/medfound/activation-objects">Activation Objects</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
---
UID: NF:wmcontainer.MFCreateASFIndexer
title: MFCreateASFIndexer function (wmcontainer.h)
description: Creates the ASF Indexer object.
helpviewer_keywords: ["MFCreateASFIndexer","MFCreateASFIndexer function [Media Foundation]","df141f8e-10b4-4ac4-8a83-c25764b8f0c6","mf.mfcreateasfindexer","wmcontainer/MFCreateASFIndexer"]
old-location: mf\mfcreateasfindexer.htm
tech.root: mf
ms.assetid: df141f8e-10b4-4ac4-8a83-c25764b8f0c6
ms.date: 12/05/2018
ms.keywords: MFCreateASFIndexer, MFCreateASFIndexer function [Media Foundation], df141f8e-10b4-4ac4-8a83-c25764b8f0c6, mf.mfcreateasfindexer, wmcontainer/MFCreateASFIndexer
req.header: wmcontainer.h
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateASFIndexer
 - wmcontainer/MFCreateASFIndexer
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
 - MFCreateASFIndexer
---

# MFCreateASFIndexer function


## -description

Creates the ASF Indexer object.

## -parameters

### -param ppIIndexer

Receives a pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer">IMFASFIndexer</a> interface. The caller must release the interface.

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
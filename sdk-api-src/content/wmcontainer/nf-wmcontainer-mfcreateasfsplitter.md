---
UID: NF:wmcontainer.MFCreateASFSplitter
title: MFCreateASFSplitter function (wmcontainer.h)
description: Creates the ASF Splitter.
helpviewer_keywords: ["05936a66-ed39-4645-adfb-5816b9981771","MFCreateASFSplitter","MFCreateASFSplitter function [Media Foundation]","mf.mfcreateasfsplitter","wmcontainer/MFCreateASFSplitter"]
old-location: mf\mfcreateasfsplitter.htm
tech.root: mf
ms.assetid: 05936a66-ed39-4645-adfb-5816b9981771
ms.date: 12/05/2018
ms.keywords: 05936a66-ed39-4645-adfb-5816b9981771, MFCreateASFSplitter, MFCreateASFSplitter function [Media Foundation], mf.mfcreateasfsplitter, wmcontainer/MFCreateASFSplitter
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
 - MFCreateASFSplitter
 - wmcontainer/MFCreateASFSplitter
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
 - MFCreateASFSplitter
---

# MFCreateASFSplitter function


## -description

Creates the <a href="/windows/desktop/medfound/asf-splitter">ASF Splitter</a>.

## -parameters

### -param ppISplitter

Receives a pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter">IMFASFSplitter</a> interface. The caller must release the interface.

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
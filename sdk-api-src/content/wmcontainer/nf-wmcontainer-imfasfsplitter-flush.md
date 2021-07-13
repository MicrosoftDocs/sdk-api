---
UID: NF:wmcontainer.IMFASFSplitter.Flush
title: IMFASFSplitter::Flush (wmcontainer.h)
description: Resets the Advanced Systems Format (ASF) splitter and releases all pending samples.
helpviewer_keywords: ["Flush","Flush method [Media Foundation]","Flush method [Media Foundation]","IMFASFSplitter interface","IMFASFSplitter interface [Media Foundation]","Flush method","IMFASFSplitter.Flush","IMFASFSplitter::Flush","be92c734-2bcb-4a7c-bd62-fb545c3c7762","mf.imfasfsplitter_flush","wmcontainer/IMFASFSplitter::Flush"]
old-location: mf\imfasfsplitter_flush.htm
tech.root: mf
ms.assetid: be92c734-2bcb-4a7c-bd62-fb545c3c7762
ms.date: 12/05/2018
ms.keywords: Flush, Flush method [Media Foundation], Flush method [Media Foundation],IMFASFSplitter interface, IMFASFSplitter interface [Media Foundation],Flush method, IMFASFSplitter.Flush, IMFASFSplitter::Flush, be92c734-2bcb-4a7c-bd62-fb545c3c7762, mf.imfasfsplitter_flush, wmcontainer/IMFASFSplitter::Flush
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFSplitter::Flush
 - wmcontainer/IMFASFSplitter::Flush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFSplitter.Flush
---

# IMFASFSplitter::Flush


## -description

Resets the Advanced Systems Format (ASF) splitter and releases all pending samples.



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
The method succeeded.

</td>
</tr>
</table>

## -remarks

Any samples waiting to be retrieved when <b>Flush</b> is called are lost.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter">IMFASFSplitter</a>

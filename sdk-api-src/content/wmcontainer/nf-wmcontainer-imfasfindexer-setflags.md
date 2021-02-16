---
UID: NF:wmcontainer.IMFASFIndexer.SetFlags
title: IMFASFIndexer::SetFlags (wmcontainer.h)
description: Sets indexer options.
helpviewer_keywords: ["7df6aba2-d63f-4a1a-b6e8-6894f92993b1","IMFASFIndexer interface [Media Foundation]","SetFlags method","IMFASFIndexer.SetFlags","IMFASFIndexer::SetFlags","SetFlags","SetFlags method [Media Foundation]","SetFlags method [Media Foundation]","IMFASFIndexer interface","mf.imfasfindexer_setflags","wmcontainer/IMFASFIndexer::SetFlags"]
old-location: mf\imfasfindexer_setflags.htm
tech.root: mf
ms.assetid: 7df6aba2-d63f-4a1a-b6e8-6894f92993b1
ms.date: 12/05/2018
ms.keywords: 7df6aba2-d63f-4a1a-b6e8-6894f92993b1, IMFASFIndexer interface [Media Foundation],SetFlags method, IMFASFIndexer.SetFlags, IMFASFIndexer::SetFlags, SetFlags, SetFlags method [Media Foundation], SetFlags method [Media Foundation],IMFASFIndexer interface, mf.imfasfindexer_setflags, wmcontainer/IMFASFIndexer::SetFlags
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
 - IMFASFIndexer::SetFlags
 - wmcontainer/IMFASFIndexer::SetFlags
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
 - IMFASFIndexer.SetFlags
---

# IMFASFIndexer::SetFlags


## -description

Sets indexer options.

## -parameters

### -param dwFlags [in]

Bitwise OR of zero or more flags from the [MFASF_INDEXER_FLAGS](./ne-wmcontainer-mfasf_indexer_flags.md) enumeration specifying the indexer options to use.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The indexer object was  initialized before setting flags for it.  For more information, see Remarks.

</td>
</tr>
</table>

## -remarks

<b>IMFASFIndexer::SetFlags</b> must be called before <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize">IMFASFIndexer::Initialize</a>. Attempting to call <b>SetFlags</b> after <b>Initialize</b> will return MF_E_INVALIDREQUEST as a result.

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer">IMFASFIndexer</a>
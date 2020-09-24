---
UID: NF:wmcontainer.IMFASFIndexer.GetFlags
title: IMFASFIndexer::GetFlags (wmcontainer.h)
description: Retrieves the flags that indicate the selected indexer options.
helpviewer_keywords: ["97809620-57ad-48f1-94ba-a2e121cdfee6","GetFlags","GetFlags method [Media Foundation]","GetFlags method [Media Foundation]","IMFASFIndexer interface","IMFASFIndexer interface [Media Foundation]","GetFlags method","IMFASFIndexer.GetFlags","IMFASFIndexer::GetFlags","mf.imfasfindexer_getflags","wmcontainer/IMFASFIndexer::GetFlags"]
old-location: mf\imfasfindexer_getflags.htm
tech.root: mf
ms.assetid: 97809620-57ad-48f1-94ba-a2e121cdfee6
ms.date: 12/05/2018
ms.keywords: 97809620-57ad-48f1-94ba-a2e121cdfee6, GetFlags, GetFlags method [Media Foundation], GetFlags method [Media Foundation],IMFASFIndexer interface, IMFASFIndexer interface [Media Foundation],GetFlags method, IMFASFIndexer.GetFlags, IMFASFIndexer::GetFlags, mf.imfasfindexer_getflags, wmcontainer/IMFASFIndexer::GetFlags
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
 - IMFASFIndexer::GetFlags
 - wmcontainer/IMFASFIndexer::GetFlags
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
 - IMFASFIndexer.GetFlags
---

# IMFASFIndexer::GetFlags


## -description

Retrieves the flags that indicate the selected indexer options.

## -parameters

### -param pdwFlags [out]

Receives a bitwise OR of zero or more flags from the [MFASF_INDEXER_FLAGS](./ne-wmcontainer-mfasf_indexer_flags.md) enumeration.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwFlags</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

You must call this method before initializing the indexer object with <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize">IMFASFIndexer::Initialize</a>.

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer">IMFASFIndexer</a>
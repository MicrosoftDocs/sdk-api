---
UID: NF:oleidl.IOleLink.GetBoundSource
title: IOleLink::GetBoundSource (oleidl.h)
description: Retrieves a pointer to the link source if the connection is active.
helpviewer_keywords: ["GetBoundSource","GetBoundSource method [COM]","GetBoundSource method [COM]","IOleLink interface","IOleLink interface [COM]","GetBoundSource method","IOleLink.GetBoundSource","IOleLink::GetBoundSource","_ole_iolelink_getboundsource","com.iolelink_getboundsource","oleidl/IOleLink::GetBoundSource"]
old-location: com\iolelink_getboundsource.htm
tech.root: com
ms.assetid: 37d24337-eacc-453a-9a90-043ec9b35e9c
ms.date: 12/05/2018
ms.keywords: GetBoundSource, GetBoundSource method [COM], GetBoundSource method [COM],IOleLink interface, IOleLink interface [COM],GetBoundSource method, IOleLink.GetBoundSource, IOleLink::GetBoundSource, _ole_iolelink_getboundsource, com.iolelink_getboundsource, oleidl/IOleLink::GetBoundSource
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleLink::GetBoundSource
 - oleidl/IOleLink::GetBoundSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleLink.GetBoundSource
---

# IOleLink::GetBoundSource


## -description

Retrieves a pointer to the link source if the connection is active.

## -parameters

### -param ppunk [out]

Address of <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> pointer variable that receives the interface pointer to the link source. When successful, the implementation must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> on <i>ppunk</i>; it is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>. If an error occurs, the implementation sets <i>ppunk</i> to <b>NULL</b>.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
</table>

## -remarks

You typically do not need to call <b>IOleLink::GetBoundSource</b>.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-iolelink">IOleLink</a>
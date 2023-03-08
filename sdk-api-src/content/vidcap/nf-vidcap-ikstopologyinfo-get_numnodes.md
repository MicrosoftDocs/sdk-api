---
UID: NF:vidcap.IKsTopologyInfo.get_NumNodes
title: IKsTopologyInfo::get_NumNodes (vidcap.h)
description: The get_NumNodes method returns the number of nodes in the filter.
helpviewer_keywords: ["IKsTopologyInfo interface [DirectShow]","get_NumNodes method","IKsTopologyInfo.get_NumNodes","IKsTopologyInfo::get_NumNodes","IKsTopologyInfoget_NumNodes","dshow.ikstopologyinfo_get_numnodes","get_NumNodes","get_NumNodes method [DirectShow]","get_NumNodes method [DirectShow]","IKsTopologyInfo interface","vidcap/IKsTopologyInfo::get_NumNodes"]
old-location: dshow\ikstopologyinfo_get_numnodes.htm
tech.root: dshow
ms.assetid: fdba99d5-fd44-4d4f-8575-867d98bf3339
ms.date: 12/05/2018
ms.keywords: IKsTopologyInfo interface [DirectShow],get_NumNodes method, IKsTopologyInfo.get_NumNodes, IKsTopologyInfo::get_NumNodes, IKsTopologyInfoget_NumNodes, dshow.ikstopologyinfo_get_numnodes, get_NumNodes, get_NumNodes method [DirectShow], get_NumNodes method [DirectShow],IKsTopologyInfo interface, vidcap/IKsTopologyInfo::get_NumNodes
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IKsTopologyInfo::get_NumNodes
 - vidcap/IKsTopologyInfo::get_NumNodes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IKsTopologyInfo.get_NumNodes
---

# IKsTopologyInfo::get_NumNodes


## -description

The <code>get_NumNodes</code> method returns the number of nodes in the filter.

## -parameters

### -param pdwNumNodes [out]

Receives the number of nodes.

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

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/windows/win32/api/vidcap/nn-vidcap-ikstopologyinfo">IKsTopologyInfo Interface</a>
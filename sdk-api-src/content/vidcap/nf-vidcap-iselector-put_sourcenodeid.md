---
UID: NF:vidcap.ISelector.put_SourceNodeId
title: ISelector::put_SourceNodeId (vidcap.h)
description: The put_SourceNodeId method activates a source node.
helpviewer_keywords: ["ISelector interface [DirectShow]","put_SourceNodeId method","ISelector.put_SourceNodeId","ISelector::put_SourceNodeId","ISelectorput_SourceNodeId","dshow.iselector_put_sourcenodeid","put_SourceNodeId","put_SourceNodeId method [DirectShow]","put_SourceNodeId method [DirectShow]","ISelector interface","vidcap/ISelector::put_SourceNodeId"]
old-location: dshow\iselector_put_sourcenodeid.htm
tech.root: dshow
ms.assetid: 6cf6a406-eeb8-45ba-9c4c-0fdc6d6a30cf
ms.date: 12/05/2018
ms.keywords: ISelector interface [DirectShow],put_SourceNodeId method, ISelector.put_SourceNodeId, ISelector::put_SourceNodeId, ISelectorput_SourceNodeId, dshow.iselector_put_sourcenodeid, put_SourceNodeId, put_SourceNodeId method [DirectShow], put_SourceNodeId method [DirectShow],ISelector interface, vidcap/ISelector::put_SourceNodeId
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
 - ISelector::put_SourceNodeId
 - vidcap/ISelector::put_SourceNodeId
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
 - ISelector.put_SourceNodeId
---

# ISelector::put_SourceNodeId


## -description

The <code>put_SourceNodeId</code> method activates a source node.

## -parameters

### -param dwPinId [in]

Index of the source node to activate.

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



<a href="/windows/desktop/api/vidcap/nn-vidcap-iselector">ISelector Interface</a>
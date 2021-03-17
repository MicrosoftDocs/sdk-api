---
UID: NF:mfidl.IMFTopologyNode.GetObject
title: IMFTopologyNode::GetObject (mfidl.h)
description: Gets the object associated with this node.
helpviewer_keywords: ["039d8009-5e5a-4503-9908-7317bc2bf412","GetObject","GetObject method [Media Foundation]","GetObject method [Media Foundation]","IMFTopologyNode interface","IMFTopologyNode interface [Media Foundation]","GetObject method","IMFTopologyNode.GetObject","IMFTopologyNode::GetObject","mf.imftopologynode_getobject","mfidl/IMFTopologyNode::GetObject"]
old-location: mf\imftopologynode_getobject.htm
tech.root: mf
ms.assetid: 039d8009-5e5a-4503-9908-7317bc2bf412
ms.date: 12/05/2018
ms.keywords: 039d8009-5e5a-4503-9908-7317bc2bf412, GetObject, GetObject method [Media Foundation], GetObject method [Media Foundation],IMFTopologyNode interface, IMFTopologyNode interface [Media Foundation],GetObject method, IMFTopologyNode.GetObject, IMFTopologyNode::GetObject, mf.imftopologynode_getobject, mfidl/IMFTopologyNode::GetObject
req.header: mfidl.h
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
 - IMFTopologyNode::GetObject
 - mfidl/IMFTopologyNode::GetObject
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
 - IMFTopologyNode.GetObject
---

# IMFTopologyNode::GetObject


## -description

Gets the object associated with this node.

## -parameters

### -param ppObject [out]

Receives a pointer to the object's <b>IUnknown</b> interface. The caller must release the interface.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There is no object associated with this node.
              

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>
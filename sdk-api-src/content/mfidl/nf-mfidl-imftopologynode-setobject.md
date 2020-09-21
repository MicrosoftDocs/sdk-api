---
UID: NF:mfidl.IMFTopologyNode.SetObject
title: IMFTopologyNode::SetObject (mfidl.h)
description: Sets the object associated with this node.
helpviewer_keywords: ["IMFTopologyNode interface [Media Foundation]","SetObject method","IMFTopologyNode.SetObject","IMFTopologyNode::SetObject","SetObject","SetObject method [Media Foundation]","SetObject method [Media Foundation]","IMFTopologyNode interface","bbef706d-a4a0-4ff3-bfdb-8ba39d70617c","mf.imftopologynode_setobject","mfidl/IMFTopologyNode::SetObject"]
old-location: mf\imftopologynode_setobject.htm
tech.root: mf
ms.assetid: bbef706d-a4a0-4ff3-bfdb-8ba39d70617c
ms.date: 12/05/2018
ms.keywords: IMFTopologyNode interface [Media Foundation],SetObject method, IMFTopologyNode.SetObject, IMFTopologyNode::SetObject, SetObject, SetObject method [Media Foundation], SetObject method [Media Foundation],IMFTopologyNode interface, bbef706d-a4a0-4ff3-bfdb-8ba39d70617c, mf.imftopologynode_setobject, mfidl/IMFTopologyNode::SetObject
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
 - IMFTopologyNode::SetObject
 - mfidl/IMFTopologyNode::SetObject
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
 - IMFTopologyNode.SetObject
---

# IMFTopologyNode::SetObject


## -description

Sets the object associated with this node.

## -parameters

### -param pObject [in]

A pointer to the object's <b>IUnknown</b> interface. Use the value <b>NULL</b> to clear an object that was previous set.

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

All node types support this method, but the object pointer is not used by every node type.

<table>
<tr>
<th>Node type</th>
<th>Object pointer</th>
</tr>
<tr>
<td>Source node.</td>
<td>Not used.</td>
</tr>
<tr>
<td>Transform node.</td>
<td>
<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a> or <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface.</td>
</tr>
<tr>
<td>Output node</td>
<td>
<a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink">IMFStreamSink</a> or <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface.</td>
</tr>
<tr>
<td>Tee node.</td>
<td>Not used.</td>
</tr>
</table>
 

If the object supports <b>IPersist</b>, <b>IPersistStorage</b>, or <b>IPersistPropertyBag</b>, the method gets the object's CLSID and sets the <a href="/windows/desktop/medfound/mf-toponode-transform-objectid-attribute">MF_TOPONODE_TRANSFORM_OBJECTID</a> attribute on the node.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>
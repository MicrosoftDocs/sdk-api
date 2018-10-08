---
UID: NF:mfidl.IMFTopologyNode.SetOutputPrefType
title: IMFTopologyNode::SetOutputPrefType
author: windows-sdk-content
description: Sets the preferred media type for an output stream on this node.
old-location: mf\imftopologynode_setoutputpreftype.htm
tech.root: medfound
ms.assetid: 948fd64d-e3d8-45de-aaab-b052d9f0b9d8
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: 948fd64d-e3d8-45de-aaab-b052d9f0b9d8, IMFTopologyNode interface [Media Foundation],SetOutputPrefType method, IMFTopologyNode.SetOutputPrefType, IMFTopologyNode::SetOutputPrefType, SetOutputPrefType, SetOutputPrefType method [Media Foundation], SetOutputPrefType method [Media Foundation],IMFTopologyNode interface, mf.imftopologynode_setoutputpreftype, mfidl/IMFTopologyNode::SetOutputPrefType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTopologyNode.SetOutputPrefType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTopologyNode::SetOutputPrefType


## -description



Sets the preferred media type for an output stream on this node.




## -parameters




### -param dwOutputIndex [in]

Zero-based index of the output stream.


### -param pType [in]

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This node is an output node.

</td>
</tr>
</table>
 




## -remarks



The preferred type is a hint for the topology loader.

Do not call this method after loading a topology or setting a topology on the Media Session. Changing the preferred type on a running topology can cause connection errors.

If no output stream exists at the specified index, the method creates new streams up to and including the specified index number.

Output nodes cannot have outputs. If this method is called on an output node, it returns E_NOTIMPL




## -see-also




<a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 


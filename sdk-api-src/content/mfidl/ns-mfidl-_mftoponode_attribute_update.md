---
UID: NS:mfidl._MFTOPONODE_ATTRIBUTE_UPDATE
title: "_MFTOPONODE_ATTRIBUTE_UPDATE"
author: windows-sdk-content
description: Specifies a new attribute value for a topology node.
old-location: mf\mftoponode_attribute_update.htm
tech.root: medfound
ms.assetid: 94c89067-9b3e-4d24-9192-a68e284c5d99
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 94c89067-9b3e-4d24-9192-a68e284c5d99, MFTOPONODE_ATTRIBUTE_UPDATE, MFTOPONODE_ATTRIBUTE_UPDATE structure [Media Foundation], _MFTOPONODE_ATTRIBUTE_UPDATE, mf.mftoponode_attribute_update, mfidl/MFTOPONODE_ATTRIBUTE_UPDATE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFTOPONODE_ATTRIBUTE_UPDATE
product: Windows
targetos: Windows
req.typenames: MFTOPONODE_ATTRIBUTE_UPDATE
req.redist: 
---

# _MFTOPONODE_ATTRIBUTE_UPDATE structure


## -description


Specifies a new attribute value for a topology node.


## -struct-fields




### -field NodeId

The identifier of the topology node to update. To get the identifier of a topology node, call <a href="https://msdn.microsoft.com/9c0e5be9-6481-4132-ad5b-9db13fb07391">IMFTopologyNode::GetTopoNodeID</a>.
          


### -field guidAttributeKey

GUID that specifies the attribute to update.
          


### -field attrType

Attribute type, specified as a member of the <a href="https://msdn.microsoft.com/1844fbe2-0a07-4c0c-9ffe-4c59fc01f793">MF_ATTRIBUTE_TYPE</a> enumeration.
          


### -field u32

Attribute value (unsigned 32-bit integer). This member is used when <b>attrType</b> equals <b>MF_ATTRIBUTE_UINT32</b>.
            


### -field u64

Attribute value (unsigned 32-bit integer). This member is used when <b>attrType</b> equals <b>MF_ATTRIBUTE_UINT64</b>. See Remarks.
            


### -field d

Attribute value (floating point). This member is used when <b>attrType</b> equals <b>MF_ATTRIBUTE_DOUBLE</b>.
            


## -remarks



Due to an error in the structure declaration, the <b>u64</b> member is declared as a 32-bit integer, not a 64-bit integer. Therefore, any 64-bit value passed to the <a href="https://msdn.microsoft.com/a769b0bd-a43f-478b-a6e4-bbef05942616">IMFTopologyNodeAttributeEditor::UpdateNodeAttributes</a> method is truncated to 32 bits.
      




## -see-also




<a href="https://msdn.microsoft.com/a769b0bd-a43f-478b-a6e4-bbef05942616">IMFTopologyNodeAttributeEditor::UpdateNodeAttributes</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/a6d9246a-0cc6-4dbd-affa-e7d0bbddb008">TOPOID</a>
 

 


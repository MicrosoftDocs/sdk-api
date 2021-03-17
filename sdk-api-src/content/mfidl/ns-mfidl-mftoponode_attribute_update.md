---
UID: NS:mfidl._MFTOPONODE_ATTRIBUTE_UPDATE
title: MFTOPONODE_ATTRIBUTE_UPDATE (mfidl.h)
description: Specifies a new attribute value for a topology node.
helpviewer_keywords: ["94c89067-9b3e-4d24-9192-a68e284c5d99","MFTOPONODE_ATTRIBUTE_UPDATE","MFTOPONODE_ATTRIBUTE_UPDATE structure [Media Foundation]","mf.mftoponode_attribute_update","mfidl/MFTOPONODE_ATTRIBUTE_UPDATE"]
old-location: mf\mftoponode_attribute_update.htm
tech.root: mf
ms.assetid: 94c89067-9b3e-4d24-9192-a68e284c5d99
ms.date: 12/05/2018
ms.keywords: 94c89067-9b3e-4d24-9192-a68e284c5d99, MFTOPONODE_ATTRIBUTE_UPDATE, MFTOPONODE_ATTRIBUTE_UPDATE structure [Media Foundation], mf.mftoponode_attribute_update, mfidl/MFTOPONODE_ATTRIBUTE_UPDATE
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
targetos: Windows
req.typenames: MFTOPONODE_ATTRIBUTE_UPDATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFTOPONODE_ATTRIBUTE_UPDATE
 - mfidl/_MFTOPONODE_ATTRIBUTE_UPDATE
 - MFTOPONODE_ATTRIBUTE_UPDATE
 - mfidl/MFTOPONODE_ATTRIBUTE_UPDATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFTOPONODE_ATTRIBUTE_UPDATE
---

# MFTOPONODE_ATTRIBUTE_UPDATE structure


## -description

Specifies a new attribute value for a topology node.

## -struct-fields

### -field NodeId

The identifier of the topology node to update. To get the identifier of a topology node, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid">IMFTopologyNode::GetTopoNodeID</a>.

### -field guidAttributeKey

GUID that specifies the attribute to update.

### -field attrType

Attribute type, specified as a member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type">MF_ATTRIBUTE_TYPE</a> enumeration.

### -field u32

Attribute value (unsigned 32-bit integer). This member is used when <b>attrType</b> equals <b>MF_ATTRIBUTE_UINT32</b>.

### -field u64

Attribute value (unsigned 32-bit integer). This member is used when <b>attrType</b> equals <b>MF_ATTRIBUTE_UINT64</b>. See Remarks.

### -field d

Attribute value (floating point). This member is used when <b>attrType</b> equals <b>MF_ATTRIBUTE_DOUBLE</b>.

## -remarks

Due to an error in the structure declaration, the <b>u64</b> member is declared as a 32-bit integer, not a 64-bit integer. Therefore, any 64-bit value passed to the <a href="/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes">IMFTopologyNodeAttributeEditor::UpdateNodeAttributes</a> method is truncated to 32 bits.

## -see-also

<a href="/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes">IMFTopologyNodeAttributeEditor::UpdateNodeAttributes</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/topoid">TOPOID</a>
---
UID: NE:wtypesbase.tagMSHLFLAGS
title: MSHLFLAGS (wtypesbase.h)
description: Specifies why the marshaling is to be done.
helpviewer_keywords: ["MSHLFLAGS","MSHLFLAGS enumeration [COM]","MSHLFLAGS_NOPING","MSHLFLAGS_NORMAL","MSHLFLAGS_TABLESTRONG","MSHLFLAGS_TABLEWEAK","_com_MSHLFLAGS","com.mshlflags","wtypesbase/MSHLFLAGS","wtypesbase/MSHLFLAGS_NOPING","wtypesbase/MSHLFLAGS_NORMAL","wtypesbase/MSHLFLAGS_TABLESTRONG","wtypesbase/MSHLFLAGS_TABLEWEAK"]
old-location: com\mshlflags.htm
tech.root: com
ms.assetid: 42a482be-d4b8-4f2e-ae43-1d210cb44c7c
ms.date: 12/05/2018
ms.keywords: MSHLFLAGS, MSHLFLAGS enumeration [COM], MSHLFLAGS_NOPING, MSHLFLAGS_NORMAL, MSHLFLAGS_TABLESTRONG, MSHLFLAGS_TABLEWEAK, _com_MSHLFLAGS, com.mshlflags, wtypesbase/MSHLFLAGS, wtypesbase/MSHLFLAGS_NOPING, wtypesbase/MSHLFLAGS_NORMAL, wtypesbase/MSHLFLAGS_TABLESTRONG, wtypesbase/MSHLFLAGS_TABLEWEAK
req.header: wtypesbase.h
req.include-header: WTypes.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MSHLFLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMSHLFLAGS
 - wtypesbase/tagMSHLFLAGS
 - MSHLFLAGS
 - wtypesbase/MSHLFLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wtypesbase.h
api_name:
 - MSHLFLAGS
---

# MSHLFLAGS enumeration


## -description

Specifies why the marshaling is to be done.

## -enum-fields

### -field MSHLFLAGS_NORMAL:0

The marshaling is occurring because an interface pointer is being passed from one process to another. This is the normal case. The data packet produced by the marshaling process will be unmarshaled in the destination process. The marshaled data packet can be unmarshaled just once, or not at all. If the receiver unmarshals the data packet successfully, the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreleasemarshaldata">CoReleaseMarshalData</a> function is automatically called on the data packet as part of the unmarshaling process. If the receiver does not or cannot unmarshal the data packet, the sender must call <b>CoReleaseMarshalData</b> on the data packet.

### -field MSHLFLAGS_TABLESTRONG:1

The marshaling is occurring because the data packet is to be stored in a globally accessible table from which it can be unmarshaled one or more times, or not at all. The presence of the data packet in the table counts as a strong reference to the interface being marshaled, meaning that it is sufficient to keep the object alive. When the data packet is removed from the table, the table implementer must call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreleasemarshaldata">CoReleaseMarshalData</a> function on the data packet.

MSHLFLAGS_TABLESTRONG is used by the <a href="/windows/desktop/api/ole2/nf-ole2-registerdragdrop">RegisterDragDrop</a> function when registering a window as a drop target. This keeps the window registered as a drop target no matter how many times the end user drags across the window. The <a href="/windows/desktop/api/ole2/nf-ole2-revokedragdrop">RevokeDragDrop</a> function calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreleasemarshaldata">CoReleaseMarshalData</a>.

### -field MSHLFLAGS_TABLEWEAK:2

The marshaling is occurring because the data packet is to be stored in a globally accessible table from which it can be unmarshaled one or more times, or not at all. However, the presence of the data packet in the table acts as a weak reference to the interface being marshaled, meaning that it is not sufficient to keep the object alive. When the data packet is removed from the table, the table implementer must call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreleasemarshaldata">CoReleaseMarshalData</a> function on the data packet. 

MSHLFLAGS_TABLEWEAK is typically used when registering an object in the running object table (ROT). This prevents the object's entry in the ROT from keeping the object alive in the absence of any other connections. See <a href="/windows/desktop/api/objidl/nf-objidl-irunningobjecttable-register">IRunningObjectTable::Register</a> for more information.

### -field MSHLFLAGS_NOPING:4

Adding this flag to an original object marshaling (as opposed to marshaling a proxy) will disable the ping protocol for that object.

### -field MSHLFLAGS_RESERVED1:8

### -field MSHLFLAGS_RESERVED2:16

### -field MSHLFLAGS_RESERVED3:32

### -field MSHLFLAGS_RESERVED4:64

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetstandardmarshal">CoGetStandardMarshal</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface">CoMarshalInterface</a>



<a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>

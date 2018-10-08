---
UID: NE:wtypesbase.tagMSHLFLAGS
title: tagMSHLFLAGS
author: windows-sdk-content
description: Specifies why the marshaling is to be done.
old-location: com\mshlflags.htm
tech.root: com
ms.assetid: 42a482be-d4b8-4f2e-ae43-1d210cb44c7c
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: MSHLFLAGS, MSHLFLAGS enumeration [COM], MSHLFLAGS_NOPING, MSHLFLAGS_NORMAL, MSHLFLAGS_TABLESTRONG, MSHLFLAGS_TABLEWEAK, _com_MSHLFLAGS, com.mshlflags, tagMSHLFLAGS, wtypesbase/MSHLFLAGS, wtypesbase/MSHLFLAGS_NOPING, wtypesbase/MSHLFLAGS_NORMAL, wtypesbase/MSHLFLAGS_TABLESTRONG, wtypesbase/MSHLFLAGS_TABLEWEAK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wtypesbase.h
api_name:
 - MSHLFLAGS
product: Windows
targetos: Windows
req.typenames: MSHLFLAGS
req.redist: 
---

# tagMSHLFLAGS enumeration


## -description


Specifies why the marshaling is to be done.


## -enum-fields




### -field MSHLFLAGS_NORMAL

The marshaling is occurring because an interface pointer is being passed from one process to another. This is the normal case. The data packet produced by the marshaling process will be unmarshaled in the destination process. The marshaled data packet can be unmarshaled just once, or not at all. If the receiver unmarshals the data packet successfully, the <a href="https://msdn.microsoft.com/a642a20f-3a3c-46bc-b833-e424dab3a16d">CoReleaseMarshalData</a> function is automatically called on the data packet as part of the unmarshaling process. If the receiver does not or cannot unmarshal the data packet, the sender must call <b>CoReleaseMarshalData</b> on the data packet.


### -field MSHLFLAGS_TABLESTRONG

The marshaling is occurring because the data packet is to be stored in a globally accessible table from which it can be unmarshaled one or more times, or not at all. The presence of the data packet in the table counts as a strong reference to the interface being marshaled, meaning that it is sufficient to keep the object alive. When the data packet is removed from the table, the table implementer must call the <a href="https://msdn.microsoft.com/a642a20f-3a3c-46bc-b833-e424dab3a16d">CoReleaseMarshalData</a> function on the data packet.

MSHLFLAGS_TABLESTRONG is used by the <a href="https://msdn.microsoft.com/00726271-4436-41f5-b7cc-666cd77216bc">RegisterDragDrop</a> function when registering a window as a drop target. This keeps the window registered as a drop target no matter how many times the end user drags across the window. The <a href="https://msdn.microsoft.com/c0fa963c-ed06-426c-8ffc-31b02f083a23">RevokeDragDrop</a> function calls <a href="https://msdn.microsoft.com/a642a20f-3a3c-46bc-b833-e424dab3a16d">CoReleaseMarshalData</a>.


### -field MSHLFLAGS_TABLEWEAK

The marshaling is occurring because the data packet is to be stored in a globally accessible table from which it can be unmarshaled one or more times, or not at all. However, the presence of the data packet in the table acts as a weak reference to the interface being marshaled, meaning that it is not sufficient to keep the object alive. When the data packet is removed from the table, the table implementer must call the <a href="https://msdn.microsoft.com/a642a20f-3a3c-46bc-b833-e424dab3a16d">CoReleaseMarshalData</a> function on the data packet. 

MSHLFLAGS_TABLEWEAK is typically used when registering an object in the running object table (ROT). This prevents the object's entry in the ROT from keeping the object alive in the absence of any other connections. See <a href="https://msdn.microsoft.com/40f815b2-dfea-416c-aae1-7ba3a710ad91">IRunningObjectTable::Register</a> for more information. 


### -field MSHLFLAGS_NOPING

Adding this flag to an original object marshaling (as opposed to marshaling a proxy) will disable the ping protocol for that object.


### -field MSHLFLAGS_RESERVED1


### -field MSHLFLAGS_RESERVED2


### -field MSHLFLAGS_RESERVED3


### -field MSHLFLAGS_RESERVED4




## -see-also




<a href="https://msdn.microsoft.com/0cb74adc-e192-4ae5-9267-02c79e301681">CoGetStandardMarshal</a>



<a href="https://msdn.microsoft.com/04ca1217-eac1-43e2-b736-8d7522ce8592">CoMarshalInterface</a>



<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>



<a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a>
 

 


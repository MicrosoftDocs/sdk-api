---
UID: NE:ifdef.IF_OPER_STATUS
title: IF_OPER_STATUS
author: windows-sdk-content
description: The IF_OPER_STATUS enumeration specifies the operational status of an interface.
old-location: iphlp\if_oper_status.htm
old-project: IpHlp
ms.assetid: 829df6fc-d5db-4efe-9c67-d0c5543dacb4
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IF_OPER_STATUS, IF_OPER_STATUS enumeration [IP Helper], IfOperStatusDormant, IfOperStatusDown, IfOperStatusLowerLayerDown, IfOperStatusNotPresent, IfOperStatusTesting, IfOperStatusUnknown, IfOperStatusUp, ifdef/IF_OPER_STATUS, ifdef/IfOperStatusDormant, ifdef/IfOperStatusDown, ifdef/IfOperStatusLowerLayerDown, ifdef/IfOperStatusNotPresent, ifdef/IfOperStatusTesting, ifdef/IfOperStatusUnknown, ifdef/IfOperStatusUp, iphlp.if_oper_status
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ifdef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IF_OPER_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ifdef.h
api_name:
-	IF_OPER_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IF_OPER_STATUS enumeration


## -description


The <b>IF_OPER_STATUS</b> enumeration specifies the operational status of an interface.


## -enum-fields




### -field IfOperStatusUp

The interface is up and operational. The interface is able to pass packets.


### -field IfOperStatusDown

The interface is not down and not operational. The interface is unable to pass packets.


### -field IfOperStatusTesting

The interface is being tested.


### -field IfOperStatusUnknown

The interface status is unknown.


### -field IfOperStatusDormant

The interface is not
   in a condition to pass packets. The interface is  not up, but is
   in a pending state, waiting for some external event.  This state identifies the situation where the
   interface is waiting for events to place it in the up state.


### -field IfOperStatusNotPresent

This state is a refinement on the down state which
   indicates that the interface is down specifically because
   some component (for example, a hardware component) is not present in
   the system.


### -field IfOperStatusLowerLayerDown

This state is a refinement on the down state.
   The interface is operational, but a networking layer below the interface is not operational.


## -remarks



The <b>IF_OPER_STATUS</b> enumeration is used in the <b>OperStatus</b> member of the <a href="https://msdn.microsoft.com/a2df3749-6c75-40c0-8952-1656bbe639a6">IP_ADAPTER_ADDRESSES</a>  structure.




## -see-also




<a href="https://msdn.microsoft.com/a2df3749-6c75-40c0-8952-1656bbe639a6">IP_ADAPTER_ADDRESSES</a>
 

 


---
UID: NE:drt.drt_leafset_key_change_type_tag
title: drt_leafset_key_change_type_tag
author: windows-driver-content
description: The DRT_LEAFSET_KEY_CHANGE_TYPE enumeration defines the set of changes that can occur on nodes in the leaf set of a locally registered key.
old-location: p2p\drt_leafset_key_change_type.htm
old-project: P2PSdk
ms.assetid: f4990710-7278-461f-a82e-94cd548eab35
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: DRT_LEAFSET_KEY_ADDED, DRT_LEAFSET_KEY_CHANGE_TYPE, DRT_LEAFSET_KEY_CHANGE_TYPE enumeration [Peer Networking], DRT_LEAFSET_KEY_DELETED, drt/DRT_LEAFSET_KEY_ADDED, drt/DRT_LEAFSET_KEY_CHANGE_TYPE, drt/DRT_LEAFSET_KEY_DELETED, drt_leafset_key_change_type_tag, p2p.drt_leafset_key_change_type
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DRT_LEAFSET_KEY_CHANGE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	drt.h
api_name:
-	DRT_LEAFSET_KEY_CHANGE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# drt_leafset_key_change_type_tag enumeration


## -description


The <b>DRT_LEAFSET_KEY_CHANGE_TYPE</b> enumeration defines  the set of   changes that can occur on nodes in the leaf set of a locally registered key.


## -enum-fields




### -field DRT_LEAFSET_KEY_ADDED

A node was added to the  DRT leaf set of the local node.


### -field DRT_LEAFSET_KEY_DELETED

A node was deleted from the  DRT leaf set of the local node.


## -remarks



This enumeration is used to determine the event type returned by <a href="https://msdn.microsoft.com/94ed3028-0bd1-449b-9902-7dbae4a70ec1">DrtGetEventData</a>, which is called with the event handle passed to <a href="https://msdn.microsoft.com/67320767-f622-478a-a886-bbea1650ac1a">DrtOpen</a>.




## -see-also




<a href="https://msdn.microsoft.com/94ed3028-0bd1-449b-9902-7dbae4a70ec1">DrtGetEventData</a>



<a href="https://msdn.microsoft.com/67320767-f622-478a-a886-bbea1650ac1a">DrtOpen</a>
 

 


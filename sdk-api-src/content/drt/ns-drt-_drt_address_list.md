---
UID: NS:drt._DRT_ADDRESS_LIST
title: "_DRT_ADDRESS_LIST"
author: windows-sdk-content
description: DRT_ADDRESS_LIST structure contains a set of DRT_ADDRESS structures that represent the nodes contacted during a search for a key.
old-location: p2p\drt_address_list.htm
old-project: P2PSdk
ms.assetid: a795dff7-4182-42ad-b14b-142a6c1312c7
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*PDRT_ADDRESS_LIST, DRT_ADDRESS_LIST, DRT_ADDRESS_LIST structure [Peer Networking], PDRT_ADDRESS_LIST, PDRT_ADDRESS_LIST structure pointer [Peer Networking], _DRT_ADDRESS_LIST, drt/DRT_ADDRESS_LIST, drt/PDRT_ADDRESS_LIST, p2p.drt_address_list"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: DRT_ADDRESS_LIST, *PDRT_ADDRESS_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	drt.h
api_name:
-	DRT_ADDRESS_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DRT_ADDRESS_LIST structure


## -description


The <b>DRT_ADDRESS_LIST</b> structure contains a set of  <a href="https://msdn.microsoft.com/d6b00d5e-14f1-4e56-b8c8-f3936f6ae9fb">DRT_ADDRESS</a> structures that represent the nodes contacted during a search for a key.


## -struct-fields




### -field AddressCount

The count of entries in <b>AddressList</b>.


### -field AddressList

An array of <a href="https://msdn.microsoft.com/d6b00d5e-14f1-4e56-b8c8-f3936f6ae9fb">DRT_ADDRESS</a> structures that contain information about addresses that participated  in the search operation.


## -see-also




<a href="https://msdn.microsoft.com/d6b00d5e-14f1-4e56-b8c8-f3936f6ae9fb">DRT_ADDRESS</a>



<a href="https://msdn.microsoft.com/b89ea470-072e-46b6-9f5d-3e05aa012188">DrtGetSearchResult</a>
 

 


---
UID: NS:stm._IPX_SERVER_ENTRY
title: "_IPX_SERVER_ENTRY"
author: windows-sdk-content
description: The IPX_SERVER_ENTRY structure describes a particular IPX service.
old-location: rras\ipx_server_entry.htm
old-project: RRAS
ms.assetid: 5b865c28-6a0e-4af3-a646-c1082b5c3ce5
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: "*PIPX_SERVER_ENTRY, IPX_SERVER_ENTRY, IPX_SERVER_ENTRY structure [RAS], PIPX_SERVER_ENTRY, PIPX_SERVER_ENTRY structure pointer [RAS], _IPX_SERVER_ENTRY, _mpr_ipx_server_entry, rras.ipx_server_entry, stm/IPX_SERVER_ENTRY, stm/PIPX_SERVER_ENTRY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: stm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: IPX_SERVER_ENTRY, *PIPX_SERVER_ENTRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Stm.h
api_name:
-	IPX_SERVER_ENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# _IPX_SERVER_ENTRY structure


## -description


The 
<b>IPX_SERVER_ENTRY</b> structure describes a particular IPX service.


## -struct-fields




### -field Type

Contains the service type as defined by the SAP specification.


### -field Name

Contains the service name as defined by SAP specifications.


### -field Network

Contains the network number portion of the service address.


### -field Node

Contains the node number portion of the service address.


### -field Socket

Contains the socket number portion of service address.


### -field HopCount

Contains the service hop count.


## -see-also




<a href="https://msdn.microsoft.com/e93e3bf2-80a2-44ec-a067-58220cdd31b4">IPX Service Table Management</a>



<a href="https://msdn.microsoft.com/37da1071-b665-405c-a4ce-f1a484aeb19b">IPX_SERVICE</a>



<a href="https://msdn.microsoft.com/c965c9d5-30bc-4755-b0bf-f59eddfe300d">Service Table Management Structures</a>
 

 


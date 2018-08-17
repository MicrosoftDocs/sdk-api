---
UID: NS:winsvc._SERVICE_PREFERRED_NODE_INFO
title: "_SERVICE_PREFERRED_NODE_INFO"
author: windows-sdk-content
description: Represents the preferred node on which to run a service.
old-location: base\service_preferred_node_info.htm
old-project: services
ms.assetid: aa16cc56-0a95-47e0-9390-c219b83aeeb4
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*LPSERVICE_PREFERRED_NODE_INFO, LPSERVICE_PREFERRED_NODE_INFO, LPSERVICE_PREFERRED_NODE_INFO structure pointer, SERVICE_PREFERRED_NODE_INFO, SERVICE_PREFERRED_NODE_INFO structure, _SERVICE_PREFERRED_NODE_INFO, base.service_preferred_node_info, winsvc/LPSERVICE_PREFERRED_NODE_INFO, winsvc/SERVICE_PREFERRED_NODE_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winsvc.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
tech.root: 
req.typenames: SERVICE_PREFERRED_NODE_INFO, *LPSERVICE_PREFERRED_NODE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsvc.h
api_name:
 - SERVICE_PREFERRED_NODE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SERVICE_PREFERRED_NODE_INFO structure


## -description


Represents the preferred node on which to run a service.


## -struct-fields




### -field usPreferredNode

The node number of the preferred node.


### -field fDelete

If this member is TRUE, the preferred node setting is deleted.


## -see-also




<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a>



<a href="https://msdn.microsoft.com/a1263968-2b26-45cc-bdd7-6aa354821a5a">NUMA Support</a>



<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a>
 

 


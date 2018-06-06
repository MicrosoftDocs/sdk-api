---
UID: NS:clusapi.CLUSPROP_LIST
title: CLUSPROP_LIST
author: windows-sdk-content
description: Accesses the beginning of a property list.
old-location: mscs\clusprop_list.htm
old-project: MsCS
ms.assetid: 1f76104f-99eb-4376-8d92-e04b7f00c46d
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PCLUSPROP_LIST, CLUSPROP_LIST, CLUSPROP_LIST structure [Failover Cluster], PCLUSPROP_LIST, PCLUSPROP_LIST structure pointer [Failover Cluster], _wolf_clusprop_list, clusapi/CLUSPROP_LIST, clusapi/PCLUSPROP_LIST, mscs.clusprop_list"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
req.typenames: CLUSPROP_LIST, *PCLUSPROP_LIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSPROP_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CLUSPROP_LIST structure


## -description


Accesses the beginning of a  <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a>.


## -struct-fields




### -field nPropertyCount

Number of properties in the property list.


### -field PropertyName

Structure describing the name of the first property in the list.


## -remarks



For information about property lists, see  <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">Property Lists</a>.




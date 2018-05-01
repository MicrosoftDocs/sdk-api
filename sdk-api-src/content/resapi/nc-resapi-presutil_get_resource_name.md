---
UID: NC:resapi.PRESUTIL_GET_RESOURCE_NAME
title: PRESUTIL_GET_RESOURCE_NAME
author: windows-driver-content
description: Returns the name of a resource. The PRESUTIL_GET_RESOURCE_NAME type defines a pointer to this function.
old-location: mscs\resutilgetresourcename.htm
old-project: MsCS
ms.assetid: 968d013f-6502-4981-982e-7b3f10c53b60
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PRESUTIL_GET_RESOURCE_NAME, PRESUTIL_GET_RESOURCE_NAME callback function [Failover Cluster], _wolf_resutilgetresourcename, mscs.resutilgetresourcename, resapi/PRESUTIL_GET_RESOURCE_NAME
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	PRESUTIL_GET_RESOURCE_NAME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PRESUTIL_GET_RESOURCE_NAME callback


## -description


Returns the name of a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. The 
    <b>PRESUTIL_GET_RESOURCE_NAME</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Resource handle (see 
      <a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>).


### -param pszResourceName [out]

Pointer to a buffer that receives the resource name.


### -param *pcchResourceNameInOut








#### - pcchResourceName [in, out]

On input, specifies the size of the buffer pointed to by <i>pszResourceName</i>, in wide 
      characters. On output, specifies the actual size of the resource name returned as a count of wide 
      characters.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




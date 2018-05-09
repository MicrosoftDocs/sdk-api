---
UID: NC:resapi.PRESUTIL_ENUM_PRIVATE_PROPERTIES
title: PRESUTIL_ENUM_PRIVATE_PROPERTIES
author: windows-driver-content
description: Retrieves the names of a cluster object's&#32;private properties. The PRESUTIL_ENUM_PRIVATE_PROPERTIES type defines a pointer to this function.
old-location: mscs\resutilenumprivateproperties.htm
old-project: MsCS
ms.assetid: 83e08a14-4f0f-4c5b-9066-53ee5bb45901
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: PRESUTIL_ENUM_PRIVATE_PROPERTIES, PRESUTIL_ENUM_PRIVATE_PROPERTIES callback, PRESUTIL_ENUM_PRIVATE_PROPERTIES callback function [Failover Cluster], _wolf_resutilenumprivateproperties, mscs.resutilenumprivateproperties, resapi/PRESUTIL_ENUM_PRIVATE_PROPERTIES
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: resapi.h
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
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	PRESUTIL_ENUM_PRIVATE_PROPERTIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PRESUTIL_ENUM_PRIVATE_PROPERTIES callback function


## -description


Retrieves the names of a  <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster object's</a> <a href="https://msdn.microsoft.com/a1dee11c-f1fe-4509-a40a-a58c4b8999ef">private properties</a>. The <b>PRESUTIL_ENUM_PRIVATE_PROPERTIES</b> type defines a pointer to this function.


## -parameters




### -param hkeyClusterKey [in]

Key identifying the location of the private properties in the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a>.


### -param pszOutProperties [out]

Pointer to an output buffer in which to receive the names of the enumerated properties.


### -param cbOutPropertiesSize [in]

Size of the output buffer pointed to by <i>pszOutProperties</i>.


### -param pcbBytesReturned [out]

Pointer to the total number of bytes returned in the output buffer.


### -param pcbRequired [out]

Pointer to the required number of bytes if the output buffer is too small to hold all of the enumerated properties.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error codes.




## -see-also




<a href="https://msdn.microsoft.com/1b3a6326-c0da-470a-9cd5-19daa9d48ccd">ResUtilEnumProperties</a>
 

 


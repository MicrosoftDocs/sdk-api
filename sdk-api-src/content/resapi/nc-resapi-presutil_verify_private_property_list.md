---
UID: NC:resapi.PRESUTIL_VERIFY_PRIVATE_PROPERTY_LIST
title: PRESUTIL_VERIFY_PRIVATE_PROPERTY_LIST
author: windows-sdk-content
description: Verifies that a property list is correctly formatted.
old-location: mscs\resutilverifyprivatepropertylist.htm
old-project: mscs
ms.assetid: 3d2eaa83-dd82-4023-8466-0131f7b90abc
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PRESUTIL_VERIFY_PRIVATE_PROPERTY_LIST, PRESUTIL_VERIFY_PRIVATE_PROPERTY_LIST callback, PRESUTIL_VERIFY_PRIVATE_PROPERTY_LIST callback function [Failover Cluster], _wolf_resutilverifyprivatepropertylist, mscs.resutilverifyprivatepropertylist, resapi/PRESUTIL_VERIFY_PRIVATE_PROPERTY_LIST
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - PRESUTIL_VERIFY_PRIVATE_PROPERTY_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PRESUTIL_VERIFY_PRIVATE_PROPERTY_LIST callback function


## -description


Verifies that a  <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a> is correctly formatted.


## -parameters




### -param pInPropertyList [in]

Pointer to an input buffer containing the property list to verify.


### -param cbInPropertyListSize [in]

Size of the input buffer pointed to by <i>pInPropertyList</i>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/18bc7455-a004-4aff-bf33-0edcb96e0cb0">ResUtilSetPrivatePropertyList</a>
 

 


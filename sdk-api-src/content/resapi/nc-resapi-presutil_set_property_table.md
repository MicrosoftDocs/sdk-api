---
UID: NC:resapi.PRESUTIL_SET_PROPERTY_TABLE
title: PRESUTIL_SET_PROPERTY_TABLE
author: windows-driver-content
description: Sets properties in the cluster database based on a property list from a property table..
old-location: mscs\resutilsetpropertytable.htm
old-project: MsCS
ms.assetid: 79d8acfa-fc5d-4810-9775-d5f065d93d6f
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: PRESUTIL_SET_PROPERTY_TABLE, PRESUTIL_SET_PROPERTY_TABLE callback, PRESUTIL_SET_PROPERTY_TABLE callback function [Failover Cluster], _wolf_resutilsetpropertytable, mscs.resutilsetpropertytable, resapi/PRESUTIL_SET_PROPERTY_TABLE
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
-	PRESUTIL_SET_PROPERTY_TABLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PRESUTIL_SET_PROPERTY_TABLE callback function


## -description


Sets properties in the 
    <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> based on a 
    <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a> from a 
    <a href="https://msdn.microsoft.com/48591d73-606b-42b4-9711-4f7a84e9e971">property table.</a>.


## -parameters




### -param hkeyClusterKey [in]

Cluster database key identifying the location of the properties to set.


### -param pPropertyTable [in]

Pointer to an array of 
      <a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a> structures describing the 
      properties to set.


### -param Reserved

Reserved.


### -param bAllowUnknownProperties [in]

Indicates whether <a href="https://msdn.microsoft.com/1a4cc421-48b0-4dbe-8a1d-778f40cb77be">unknown properties</a> should be 
      accepted. This parameter is set to <b>TRUE</b> if they should be accepted, and 
      <b>FALSE</b> if not.


### -param pInPropertyList [in]

Pointer to the input buffer containing a property list.


### -param cbInPropertyListSize [in]

Size in bytes of the input buffer pointed to by <i>cbInPropertyList</i>.


### -param pOutParams [out, optional]

Pointer to a <a href="https://msdn.microsoft.com/fd77397b-36dd-4a20-b3f4-7dbbee1fd787">parameter block</a> to hold returned data. 
      If specified, parameters are only written if they differ from those in the input buffer.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error 
       codes.




## -remarks



If a value specified in the property table already exists in the cluster database, the value is not written. 
    For information on forcing all values to be written, see 
    <a href="https://msdn.microsoft.com/82f5f5d5-8ec1-4693-b66c-f141a8999803">ResUtilSetPropertyTableEx</a>.

Do not call <i>ResUtilSetPropertyTable</i> from the following resource DLL entry 
    point functions.

<ul>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a>
</li>
</ul>
<i>ResUtilSetPropertyTable</i> can be safely called from any other resource DLL 
    entry point function or from a worker thread. For more information, see 
    <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a>



<a href="https://msdn.microsoft.com/82f5f5d5-8ec1-4693-b66c-f141a8999803">ResUtilSetPropertyTableEx</a>
 

 


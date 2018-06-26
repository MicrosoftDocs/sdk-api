---
UID: NC:resapi.PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX
title: PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX
author: windows-sdk-content
description: Sets properties in the cluster database from a parameter block.
old-location: mscs\resutilsetpropertyparameterblockex.htm
old-project: MsCS
ms.assetid: aeb53528-56bf-4330-ad43-22f1381df109
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX, PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX callback, PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX callback function [Failover Cluster], _wolf_resutilsetpropertyparameterblockex, mscs.resutilsetpropertyparameterblockex, resapi/PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX
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
 - PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX callback function


## -description


Sets properties in the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> from a  <a href="https://msdn.microsoft.com/fd77397b-36dd-4a20-b3f4-7dbbee1fd787">parameter block</a>.


## -parameters




### -param hkeyClusterKey [in]

Cluster database key identifying the location for the properties to set.


### -param pPropertyTable [in]

Pointer to an array of  <a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a> structures describing the properties to set.


### -param Reserved [in]

Reserved.


### -param pInParams [in]

Pointer to an input parameter block containing the data for the properties described in the  <a href="https://msdn.microsoft.com/48591d73-606b-42b4-9711-4f7a84e9e971">property table</a> pointed to by <i>pPropertyTable</i>.


### -param pInPropertyList [in]

Pointer to the input buffer containing a  <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a> or <b>NULL</b>. If <i>pInPropertyList</i> is not <b>NULL</b>, any properties listed in the property list that are not listed in the property table are also set in the cluster database.


### -param cbInPropertyListSize [in]

Size in bytes of the input buffer pointed to by <i>pInPropertyList</i>.


### -param bForceWrite [in]

Forces the property values to be written to the cluster database even if the new values are identical to the existing values


### -param pOutParams [out, optional]

Pointer to a parameter block to receive data copied from the <i>pInParams</i> parameter.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error codes.




## -remarks



Do not call  <i>ResUtilSetPropertyParameterBlockEx</i> from the following resource DLL entry point functions:

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
<i>ResUtilSetPropertyParameterBlockEx</i> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a>



<a href="https://msdn.microsoft.com/a8d4162b-fe4e-4915-8102-744d964a6c83">ResUtilSetPropertyParameterBlock</a>
 

 


---
UID: NF:resapi.ResUtilSetUnknownProperties
title: ResUtilSetUnknownProperties function
author: windows-sdk-content
description: Stores a cluster object's unknown properties in the cluster database.
old-location: mscs\resutilsetunknownproperties.htm
tech.root: mscs
ms.assetid: ee729a3d-9d10-459c-b57d-de17f29d8ae8
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: PRESUTIL_SET_UNKNOWN_PROPERTIES, PRESUTIL_SET_UNKNOWN_PROPERTIES function [Failover Cluster], ResUtilSetUnknownProperties, ResUtilSetUnknownProperties function [Failover Cluster], _wolf_resutilsetunknownproperties, mscs.resutilsetunknownproperties, resapi/PRESUTIL_SET_UNKNOWN_PROPERTIES, resapi/ResUtilSetUnknownProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilSetUnknownProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilSetUnknownProperties function


## -description


Stores a  <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster object's</a> unknown properties in the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a>.


## -parameters




### -param hkeyClusterKey [in]


<a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">Cluster database</a> key identifying the location of the properties to set.


### -param pPropertyTable [in]

Pointer to a  <a href="https://msdn.microsoft.com/48591d73-606b-42b4-9711-4f7a84e9e971">property table</a> specifying properties that should NOT be set by this function.


### -param pInPropertyList [in]

Pointer to a  <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a>. Any properties that appear in this list and that do NOT appear in <i>pInPropertyList</i> are set.


### -param cbInPropertyListSize [in]

Pointer to the size in bytes of the input buffer pointed to by <i>pInPropertyList</i>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



<b>ResUtilSetUnknownProperties</b> only sets the properties listed in <i>pInPropertyList</i> that are NOT listed in <i>pPropertyTable</i>.

Use the  <a href="https://msdn.microsoft.com/17659c86-d7cc-4316-ba0e-ce71de727fa1">ResUtilAddUnknownProperties</a> to create the property list and  <a href="https://msdn.microsoft.com/18a27e1c-e709-4b0a-97c1-b0697deb8dc7">ResUtilGetAllProperties</a> to retrieve  <a href="https://msdn.microsoft.com/1a4cc421-48b0-4dbe-8a1d-778f40cb77be">unknown properties</a>.

Do not call  <b>ResUtilSetUnknownProperties</b> from the following resource DLL entry point functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/c7c74440-c98a-4440-8bf4-10ebd1a68608">Close</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1d67a4f5-66f8-4818-8b63-d0f50452f889">Offline</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b406ef44-0622-4625-a6cf-462b6ea6018d">Online</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0a5c10c5-0380-4638-b49d-396be3b3c0dd">Open</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a>
</li>
</ul>
<b>ResUtilSetUnknownProperties</b> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/17659c86-d7cc-4316-ba0e-ce71de727fa1">ResUtilAddUnknownProperties</a>



<a href="https://msdn.microsoft.com/18a27e1c-e709-4b0a-97c1-b0697deb8dc7">ResUtilGetAllProperties</a>
 

 


---
UID: NF:resapi.ResUtilSetPropertyParameterBlockEx
title: ResUtilSetPropertyParameterBlockEx function (resapi.h)
author: windows-sdk-content
description: Sets properties in the cluster database from a parameter block.
old-location: mscs\resutilsetpropertyparameterblockex.htm
tech.root: MsCS
ms.assetid: aeb53528-56bf-4330-ad43-22f1381df109
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX, PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX function [Failover Cluster], ResUtilSetPropertyParameterBlockEx, ResUtilSetPropertyParameterBlockEx function [Failover Cluster], _wolf_resutilsetpropertyparameterblockex, mscs.resutilsetpropertyparameterblockex, resapi/PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX, resapi/ResUtilSetPropertyParameterBlockEx
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
 - ResUtilSetPropertyParameterBlockEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ResUtilSetPropertyParameterBlockEx function


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

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The syntax, format, or type of a property in the property table pointed to by <i>pPropertyTable</i> is incorrect, or a property is  <a href="https://msdn.microsoft.com/7df0981b-7253-40c1-9a5d-44cfc4cdf13b">read-only</a> and cannot be updated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_ARGUMENTS</b></dt>
</dl>
</td>
<td width="60%">
One or more of the input parameters were invalid.

</td>
</tr>
</table>
 




## -remarks



Do not call  <b>ResUtilSetPropertyParameterBlockEx</b> from the following resource DLL entry point functions:

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
<b>ResUtilSetPropertyParameterBlockEx</b> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a>



<a href="https://msdn.microsoft.com/a8d4162b-fe4e-4915-8102-744d964a6c83">ResUtilSetPropertyParameterBlock</a>
 

 


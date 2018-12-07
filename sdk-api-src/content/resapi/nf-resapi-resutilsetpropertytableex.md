---
UID: NF:resapi.ResUtilSetPropertyTableEx
title: ResUtilSetPropertyTableEx function
author: windows-sdk-content
description: Sets properties in the cluster database based on a property list from a property table.
old-location: mscs\resutilsetpropertytableex.htm
tech.root: mscs
ms.assetid: 82f5f5d5-8ec1-4693-b66c-f141a8999803
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PRESUTIL_SET_PROPERTY_TABLE_EX, PRESUTIL_SET_PROPERTY_TABLE_EX function [Failover Cluster], ResUtilSetPropertyTableEx, ResUtilSetPropertyTableEx function [Failover Cluster], _wolf_resutilsetpropertytableex, mscs.resutilsetpropertytableex, resapi/PRESUTIL_SET_PROPERTY_TABLE_EX, resapi/ResUtilSetPropertyTableEx
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
 - ResUtilSetPropertyTableEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilSetPropertyTableEx function


## -description


Sets properties in the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> based on a  <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a> from a  <a href="https://msdn.microsoft.com/48591d73-606b-42b4-9711-4f7a84e9e971">property table</a>.


## -parameters




### -param hkeyClusterKey [in]

Cluster database key identifying the location of the properties to set.


### -param pPropertyTable [in]

Pointer to an array of  <a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a> structures describing the properties to set.


### -param Reserved

Reserved.


### -param bAllowUnknownProperties [in]

Indicates whether  <a href="https://msdn.microsoft.com/1a4cc421-48b0-4dbe-8a1d-778f40cb77be">unknown properties</a> should be accepted. This parameter is set to <b>TRUE</b> if they should be accepted and <b>FALSE</b> if not.


### -param pInPropertyList [in]

Pointer to the input buffer containing a property list.


### -param cbInPropertyListSize [in]

Size in bytes of the input buffer pointed to by <i>cbInPropertyList</i>.


### -param bForceWrite [in]

Forces the property values to be written to the cluster database even if the new values are identical to the existing values


### -param pOutParams [out, optional]

Pointer to a  <a href="https://msdn.microsoft.com/fd77397b-36dd-4a20-b3f4-7dbbee1fd787">parameter block</a> to hold returned data. When this is pointer is specified, only parameters that differ from those in the input buffer are written to the parameter block.


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
<dt><b>ERROR_BAD_ARGUMENTS</b></dt>
</dl>
</td>
<td width="60%">
One or more of the input parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of the input buffer specified in <i>cbInPropertyListSize</i> is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The input buffer pointed to by <i>pInPropertyList</i> is <b>NULL</b>, a property name is not valid, or a property value is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The syntax, format, or type of a property in the property table pointed to by <i>pPropertyTable</i> is incorrect, or a property is read-only and cannot be set.

</td>
</tr>
</table>
 




## -remarks



Do not call  <b>ResUtilSetPropertyTableEx</b> from the following resource DLL entry point functions:

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
<b>ResUtilSetPropertyTableEx</b> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a>



<a href="https://msdn.microsoft.com/79d8acfa-fc5d-4810-9775-d5f065d93d6f">ResUtilSetPropertyTable</a>
 

 


---
UID: NF:resapi.ResUtilSetPrivatePropertyList
title: ResUtilSetPrivatePropertyList function
author: windows-sdk-content
description: Sets the private properties of a cluster object.
old-location: mscs\resutilsetprivatepropertylist.htm
tech.root: mscs
ms.assetid: 18bc7455-a004-4aff-bf33-0edcb96e0cb0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PRESUTIL_SET_PRIVATE_PROPERTY_LIST, PRESUTIL_SET_PRIVATE_PROPERTY_LIST function [Failover Cluster], ResUtilSetPrivatePropertyList, ResUtilSetPrivatePropertyList function [Failover Cluster], _wolf_resutilsetprivatepropertylist, mscs.resutilsetprivatepropertylist, resapi/PRESUTIL_SET_PRIVATE_PROPERTY_LIST, resapi/ResUtilSetPrivatePropertyList
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
 - ResUtilSetPrivatePropertyList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilSetPrivatePropertyList function


## -description


Sets the  <a href="https://msdn.microsoft.com/a1dee11c-f1fe-4509-a40a-a58c4b8999ef">private properties</a> of a  <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster object</a>.


## -parameters




### -param hkeyClusterKey [in]


<a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">Cluster database</a> key identifying the location of the properties to set.


### -param pInPropertyList [in]

Pointer to an input buffer containing a  <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a> with the names and values of the properties to set.


### -param cbInPropertyListSize [in]

Pointer to the size in bytes of the input buffer pointed to by <i>pInPropertyList</i>.


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
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
There was a problem with the length of a property's data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The input buffer pointed to by <i>pInPropertyList</i> was NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The syntax of a property name was invalid.

</td>
</tr>
</table>
 




## -remarks



The properties that are set in the  <b>ResUtilSetPrivatePropertyList</b> utility function are placed in the portion of the cluster database below the specified key for the object exactly as specified by the names in the property list. If the name of a property contains backslash characters (\), each string preceding a backslash character is interpreted as a subkey name, and the last string following the last backslash character is interpreted as the value name.

Do not call  <b>ResUtilSetPrivatePropertyList</b> from the following resource DLL entry point functions:

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
<b>ResUtilSetPrivatePropertyList</b> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/3d2eaa83-dd82-4023-8466-0131f7b90abc">ResUtilVerifyPrivatePropertyList</a>
 

 


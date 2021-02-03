---
UID: NF:resapi.ResUtilSetPrivatePropertyList
title: ResUtilSetPrivatePropertyList function (resapi.h)
description: Sets the private properties of a cluster object.
helpviewer_keywords: ["PRESUTIL_SET_PRIVATE_PROPERTY_LIST","PRESUTIL_SET_PRIVATE_PROPERTY_LIST function [Failover Cluster]","ResUtilSetPrivatePropertyList","ResUtilSetPrivatePropertyList function [Failover Cluster]","_wolf_resutilsetprivatepropertylist","mscs.resutilsetprivatepropertylist","resapi/PRESUTIL_SET_PRIVATE_PROPERTY_LIST","resapi/ResUtilSetPrivatePropertyList"]
old-location: mscs\resutilsetprivatepropertylist.htm
tech.root: MsCS
ms.assetid: 18bc7455-a004-4aff-bf33-0edcb96e0cb0
ms.date: 12/05/2018
ms.keywords: PRESUTIL_SET_PRIVATE_PROPERTY_LIST, PRESUTIL_SET_PRIVATE_PROPERTY_LIST function [Failover Cluster], ResUtilSetPrivatePropertyList, ResUtilSetPrivatePropertyList function [Failover Cluster], _wolf_resutilsetprivatepropertylist, mscs.resutilsetprivatepropertylist, resapi/PRESUTIL_SET_PRIVATE_PROPERTY_LIST, resapi/ResUtilSetPrivatePropertyList
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilSetPrivatePropertyList
 - resapi/ResUtilSetPrivatePropertyList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilSetPrivatePropertyList
---

# ResUtilSetPrivatePropertyList function


## -description

Sets the  <a href="/previous-versions/windows/desktop/mscs/private-properties">private properties</a> of a  <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster object</a>.

## -parameters

### -param hkeyClusterKey [in]

<a href="/previous-versions/windows/desktop/mscs/cluster-database">Cluster database</a> key identifying the location of the properties to set.

### -param pInPropertyList [in]

Pointer to an input buffer containing a  <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a> with the names and values of the properties to set.

### -param cbInPropertyListSize [in]

Pointer to the size in bytes of the input buffer pointed to by <i>pInPropertyList</i>.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following are possible error codes.

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

The properties that are set in the  <b>ResUtilSetPrivatePropertyList</b> utility function are placed in the portion of the cluster database below the specified key for the object exactly as specified by the names in the property list. If the name of a property contains backslash characters (\\), each string preceding a backslash character is interpreted as a subkey name, and the last string following the last backslash character is interpreted as the value name.

Do not call  <b>ResUtilSetPrivatePropertyList</b> from the following resource DLL entry point functions:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pclose_routine">Close</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a>
</li>
</ul>
<b>ResUtilSetPrivatePropertyList</b> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutilverifyprivatepropertylist">ResUtilVerifyPrivatePropertyList</a>
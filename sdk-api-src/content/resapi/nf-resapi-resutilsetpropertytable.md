---
UID: NF:resapi.ResUtilSetPropertyTable
title: ResUtilSetPropertyTable function (resapi.h)
description: Sets properties in the cluster database based on a property list from a property table..
helpviewer_keywords: ["PRESUTIL_SET_PROPERTY_TABLE","PRESUTIL_SET_PROPERTY_TABLE function [Failover Cluster]","ResUtilSetPropertyTable","ResUtilSetPropertyTable function [Failover Cluster]","_wolf_resutilsetpropertytable","mscs.resutilsetpropertytable","resapi/PRESUTIL_SET_PROPERTY_TABLE","resapi/ResUtilSetPropertyTable"]
old-location: mscs\resutilsetpropertytable.htm
tech.root: MsCS
ms.assetid: 79d8acfa-fc5d-4810-9775-d5f065d93d6f
ms.date: 12/05/2018
ms.keywords: PRESUTIL_SET_PROPERTY_TABLE, PRESUTIL_SET_PROPERTY_TABLE function [Failover Cluster], ResUtilSetPropertyTable, ResUtilSetPropertyTable function [Failover Cluster], _wolf_resutilsetpropertytable, mscs.resutilsetpropertytable, resapi/PRESUTIL_SET_PROPERTY_TABLE, resapi/ResUtilSetPropertyTable
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
 - ResUtilSetPropertyTable
 - resapi/ResUtilSetPropertyTable
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
 - ResUtilSetPropertyTable
---

# ResUtilSetPropertyTable function


## -description

Sets properties in the 
    <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> based on a 
    <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a> from a 
    <a href="/previous-versions/windows/desktop/mscs/property-tables">property table.</a>.

## -parameters

### -param hkeyClusterKey [in]

Cluster database key identifying the location of the properties to set.

### -param pPropertyTable [in]

Pointer to an array of 
      <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a> structures describing the 
      properties to set.

### -param Reserved

Reserved.

### -param bAllowUnknownProperties [in]

Indicates whether <a href="/previous-versions/windows/desktop/mscs/unknown-properties">unknown properties</a> should be 
      accepted. This parameter is set to <b>TRUE</b> if they should be accepted, and 
      <b>FALSE</b> if not.

### -param pInPropertyList [in]

Pointer to the input buffer containing a property list.

### -param cbInPropertyListSize [in]

Size in bytes of the input buffer pointed to by <i>cbInPropertyList</i>.

### -param pOutParams [out, optional]

Pointer to a <a href="/previous-versions/windows/desktop/mscs/parameter-blocks">parameter block</a> to hold returned data. 
      If specified, parameters are only written if they differ from those in the input buffer.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following are possible error 
       codes.

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
The size of the input buffer specified in <i>cbInPropertyListSize</i> is too 
        small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The input buffer pointed to by <i>pInPropertyList</i> is 
        <b>NULL</b>, a property name is not valid, or a property value is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The syntax, format, or type of a property in the property table pointed to by 
        <i>pPropertyTable</i> is incorrect, or a property is 
        <a href="/previous-versions/windows/desktop/mscs/read-only-properties">read-only</a> and cannot be set.

</td>
</tr>
</table>

## -remarks

If a value specified in the property table already exists in the cluster database, the value is not written. 
    For information on forcing all values to be written, see 
    <a href="/windows/desktop/api/resapi/nf-resapi-resutilsetpropertytableex">ResUtilSetPropertyTableEx</a>.

Do not call <b>ResUtilSetPropertyTable</b> from the following resource DLL entry 
    point functions.

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
<b>ResUtilSetPropertyTable</b> can be safely called from any other resource DLL 
    entry point function or from a worker thread. For more information, see 
    <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetpropertytableex">ResUtilSetPropertyTableEx</a>
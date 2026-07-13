---
UID: NF:resapi.ResUtilSetPropertyParameterBlockEx
title: ResUtilSetPropertyParameterBlockEx function (resapi.h)
description: Sets properties in the cluster database from a parameter block. (ResUtilSetPropertyParameterBlockEx)
helpviewer_keywords: ["PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX","PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX function [Failover Cluster]","ResUtilSetPropertyParameterBlockEx","ResUtilSetPropertyParameterBlockEx function [Failover Cluster]","_wolf_resutilsetpropertyparameterblockex","mscs.resutilsetpropertyparameterblockex","resapi/PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX","resapi/ResUtilSetPropertyParameterBlockEx"]
old-location: mscs\resutilsetpropertyparameterblockex.htm
tech.root: MsCS
ms.assetid: aeb53528-56bf-4330-ad43-22f1381df109
ms.date: 12/05/2018
ms.keywords: PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX, PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX function [Failover Cluster], ResUtilSetPropertyParameterBlockEx, ResUtilSetPropertyParameterBlockEx function [Failover Cluster], _wolf_resutilsetpropertyparameterblockex, mscs.resutilsetpropertyparameterblockex, resapi/PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK_EX, resapi/ResUtilSetPropertyParameterBlockEx
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
 - ResUtilSetPropertyParameterBlockEx
 - resapi/ResUtilSetPropertyParameterBlockEx
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
 - ResUtilSetPropertyParameterBlockEx
---

# ResUtilSetPropertyParameterBlockEx function


## -description

Sets properties in the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> from a  <a href="/previous-versions/windows/desktop/mscs/parameter-blocks">parameter block</a>.

## -parameters

### -param hkeyClusterKey [in]

Cluster database key identifying the location for the properties to set.

### -param pPropertyTable [in]

Pointer to an array of  <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a> structures describing the properties to set.

### -param Reserved [in]

Reserved.

### -param pInParams [in]

Pointer to an input parameter block containing the data for the properties described in the  <a href="/previous-versions/windows/desktop/mscs/property-tables">property table</a> pointed to by <i>pPropertyTable</i>.

### -param pInPropertyList [in]

Pointer to the input buffer containing a  <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a> or <b>NULL</b>. If <i>pInPropertyList</i> is not <b>NULL</b>, any properties listed in the property list that are not listed in the property table are also set in the cluster database.

### -param cbInPropertyListSize [in]

Size in bytes of the input buffer pointed to by <i>pInPropertyList</i>.

### -param bForceWrite [in]

Forces the property values to be written to the cluster database even if the new values are identical to the existing values

### -param pOutParams [out, optional]

Pointer to a parameter block to receive data copied from the <i>pInParams</i> parameter.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The syntax, format, or type of a property in the property table pointed to by <i>pPropertyTable</i> is incorrect, or a property is  <a href="/previous-versions/windows/desktop/mscs/read-only-properties">read-only</a> and cannot be updated.

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
<b>ResUtilSetPropertyParameterBlockEx</b> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetpropertyparameterblock">ResUtilSetPropertyParameterBlock</a>

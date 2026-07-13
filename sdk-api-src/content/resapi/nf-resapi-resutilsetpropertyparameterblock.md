---
UID: NF:resapi.ResUtilSetPropertyParameterBlock
title: ResUtilSetPropertyParameterBlock function (resapi.h)
description: Sets properties in the cluster database from a parameter block. (ResUtilSetPropertyParameterBlock)
helpviewer_keywords: ["PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK","PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK function [Failover Cluster]","ResUtilSetPropertyParameterBlock","ResUtilSetPropertyParameterBlock function [Failover Cluster]","_wolf_resutilsetpropertyparameterblock","mscs.resutilsetpropertyparameterblock","resapi/PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK","resapi/ResUtilSetPropertyParameterBlock"]
old-location: mscs\resutilsetpropertyparameterblock.htm
tech.root: MsCS
ms.assetid: a8d4162b-fe4e-4915-8102-744d964a6c83
ms.date: 12/05/2018
ms.keywords: PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK, PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK function [Failover Cluster], ResUtilSetPropertyParameterBlock, ResUtilSetPropertyParameterBlock function [Failover Cluster], _wolf_resutilsetpropertyparameterblock, mscs.resutilsetpropertyparameterblock, resapi/PRESUTIL_SET_PROPERTY_PARAMETER_BLOCK, resapi/ResUtilSetPropertyParameterBlock
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
 - ResUtilSetPropertyParameterBlock
 - resapi/ResUtilSetPropertyParameterBlock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-resutils-l1-1-3.dll
 - ResUtils.dll
api_name:
 - ResUtilSetPropertyParameterBlock
---

# ResUtilSetPropertyParameterBlock function


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
The syntax, format, or type of a property in the property table pointed to by <i>pPropertyTable</i> is incorrect, or a property is read-only and cannot be updated.

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

If a value specified in the parameter block already exists in the cluster database, the value is not written. To force all values to be written, see  <a href="/windows/desktop/api/resapi/nf-resapi-resutilsetpropertyparameterblockex">ResUtilSetPropertyParameterBlockEx</a>.

Do not call  <b>ResUtilSetPropertyParameterBlock</b> from the following resource DLL entry point functions:

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
<b>ResUtilSetPropertyParameterBlock</b> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a>

---
UID: NF:resapi.ResUtilSetUnknownProperties
title: ResUtilSetUnknownProperties function (resapi.h)
description: Stores a cluster object's unknown properties in the cluster database.
helpviewer_keywords: ["PRESUTIL_SET_UNKNOWN_PROPERTIES","PRESUTIL_SET_UNKNOWN_PROPERTIES function [Failover Cluster]","ResUtilSetUnknownProperties","ResUtilSetUnknownProperties function [Failover Cluster]","_wolf_resutilsetunknownproperties","mscs.resutilsetunknownproperties","resapi/PRESUTIL_SET_UNKNOWN_PROPERTIES","resapi/ResUtilSetUnknownProperties"]
old-location: mscs\resutilsetunknownproperties.htm
tech.root: MsCS
ms.assetid: ee729a3d-9d10-459c-b57d-de17f29d8ae8
ms.date: 12/05/2018
ms.keywords: PRESUTIL_SET_UNKNOWN_PROPERTIES, PRESUTIL_SET_UNKNOWN_PROPERTIES function [Failover Cluster], ResUtilSetUnknownProperties, ResUtilSetUnknownProperties function [Failover Cluster], _wolf_resutilsetunknownproperties, mscs.resutilsetunknownproperties, resapi/PRESUTIL_SET_UNKNOWN_PROPERTIES, resapi/ResUtilSetUnknownProperties
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
 - ResUtilSetUnknownProperties
 - resapi/ResUtilSetUnknownProperties
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
 - ResUtilSetUnknownProperties
---

# ResUtilSetUnknownProperties function


## -description

Stores a  <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster object's</a> unknown properties in the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>.

## -parameters

### -param hkeyClusterKey [in]

<a href="/previous-versions/windows/desktop/mscs/cluster-database">Cluster database</a> key identifying the location of the properties to set.

### -param pPropertyTable [in]

Pointer to a  <a href="/previous-versions/windows/desktop/mscs/property-tables">property table</a> specifying properties that should NOT be set by this function.

### -param pInPropertyList [in]

Pointer to a  <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a>. Any properties that appear in this list and that do NOT appear in <i>pInPropertyList</i> are set.

### -param cbInPropertyListSize [in]

Pointer to the size in bytes of the input buffer pointed to by <i>pInPropertyList</i>.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

<b>ResUtilSetUnknownProperties</b> only sets the properties listed in <i>pInPropertyList</i> that are NOT listed in <i>pPropertyTable</i>.

Use the  <a href="/windows/desktop/api/resapi/nf-resapi-resutiladdunknownproperties">ResUtilAddUnknownProperties</a> to create the property list and  <a href="/windows/desktop/api/resapi/nf-resapi-resutilgetallproperties">ResUtilGetAllProperties</a> to retrieve  <a href="/previous-versions/windows/desktop/mscs/unknown-properties">unknown properties</a>.

Do not call  <b>ResUtilSetUnknownProperties</b> from the following resource DLL entry point functions:

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
<b>ResUtilSetUnknownProperties</b> can be safely called from any other resource DLL entry point function or from a worker thread. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutiladdunknownproperties">ResUtilAddUnknownProperties</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetallproperties">ResUtilGetAllProperties</a>
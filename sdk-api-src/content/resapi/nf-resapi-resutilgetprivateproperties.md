---
UID: NF:resapi.ResUtilGetPrivateProperties
title: ResUtilGetPrivateProperties function (resapi.h)
description: Returns private properties for a cluster object. The PRESUTIL_GET_PRIVATE_PROPERTIES type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_PRIVATE_PROPERTIES","PRESUTIL_GET_PRIVATE_PROPERTIES function [Failover Cluster]","ResUtilGetPrivateProperties","ResUtilGetPrivateProperties function [Failover Cluster]","_wolf_resutilgetprivateproperties","mscs.resutilgetprivateproperties","resapi/PRESUTIL_GET_PRIVATE_PROPERTIES","resapi/ResUtilGetPrivateProperties"]
old-location: mscs\resutilgetprivateproperties.htm
tech.root: MsCS
ms.assetid: 84019a77-4ecd-4618-ab7d-458c6c855dfd
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_PRIVATE_PROPERTIES, PRESUTIL_GET_PRIVATE_PROPERTIES function [Failover Cluster], ResUtilGetPrivateProperties, ResUtilGetPrivateProperties function [Failover Cluster], _wolf_resutilgetprivateproperties, mscs.resutilgetprivateproperties, resapi/PRESUTIL_GET_PRIVATE_PROPERTIES, resapi/ResUtilGetPrivateProperties
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
 - ResUtilGetPrivateProperties
 - resapi/ResUtilGetPrivateProperties
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
 - ResUtilGetPrivateProperties
---

# ResUtilGetPrivateProperties function


## -description

Returns  <a href="/previous-versions/windows/desktop/mscs/private-properties">private properties</a> for a  <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster object</a>. The <b>PRESUTIL_GET_PRIVATE_PROPERTIES</b> type defines a pointer to this function.

## -parameters

### -param hkeyClusterKey [in]

Pointer to the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key that identifies the location of the private properties to retrieve.

### -param pOutPropertyList [out]

Pointer to an output buffer in which a  <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a> with the names and values of the private properties is returned.

### -param cbOutPropertyListSize [in]

Size of the output buffer pointed to by <i>pOutPropertyList</i>.

### -param pcbBytesReturned [out]

Pointer to the total number of bytes in the property list pointed to by <i>pOutPropertyList</i>.

### -param pcbRequired [out]

Pointer to the number of bytes that is required if <i>pOutPropertyList</i> is too small to hold all of the private properties.

## -returns

If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was an error allocating memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The size of the output buffer is too small to hold the resulting data. The <i>pcbRequired</i> parameter points to the correct size.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetproperties">ResUtilGetProperties</a>
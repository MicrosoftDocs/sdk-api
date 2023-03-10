---
UID: NF:resapi.ResUtilEnumPrivateProperties
title: ResUtilEnumPrivateProperties function (resapi.h)
description: Retrieves the names of a cluster object's private properties. The PRESUTIL_ENUM_PRIVATE_PROPERTIES type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_ENUM_PRIVATE_PROPERTIES","PRESUTIL_ENUM_PRIVATE_PROPERTIES function [Failover Cluster]","ResUtilEnumPrivateProperties","ResUtilEnumPrivateProperties function [Failover Cluster]","_wolf_resutilenumprivateproperties","mscs.resutilenumprivateproperties","resapi/PRESUTIL_ENUM_PRIVATE_PROPERTIES","resapi/ResUtilEnumPrivateProperties"]
old-location: mscs\resutilenumprivateproperties.htm
tech.root: MsCS
ms.assetid: 83e08a14-4f0f-4c5b-9066-53ee5bb45901
ms.date: 12/05/2018
ms.keywords: PRESUTIL_ENUM_PRIVATE_PROPERTIES, PRESUTIL_ENUM_PRIVATE_PROPERTIES function [Failover Cluster], ResUtilEnumPrivateProperties, ResUtilEnumPrivateProperties function [Failover Cluster], _wolf_resutilenumprivateproperties, mscs.resutilenumprivateproperties, resapi/PRESUTIL_ENUM_PRIVATE_PROPERTIES, resapi/ResUtilEnumPrivateProperties
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
 - ResUtilEnumPrivateProperties
 - resapi/ResUtilEnumPrivateProperties
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
 - ResUtilEnumPrivateProperties
---

# ResUtilEnumPrivateProperties function


## -description

Retrieves the names of a  <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster object's</a> <a href="/previous-versions/windows/desktop/mscs/private-properties">private properties</a>. The <b>PRESUTIL_ENUM_PRIVATE_PROPERTIES</b> type defines a pointer to this function.

## -parameters

### -param hkeyClusterKey [in]

Key identifying the location of the private properties in the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>.

### -param pszOutProperties [out]

Pointer to an output buffer in which to receive the names of the enumerated properties.

### -param cbOutPropertiesSize [in]

Size of the output buffer pointed to by <i>pszOutProperties</i>.

### -param pcbBytesReturned [out]

Pointer to the total number of bytes returned in the output buffer.

### -param pcbRequired [out]

Pointer to the required number of bytes if the output buffer is too small to hold all of the enumerated properties.

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

<a href="/windows/desktop/api/resapi/nf-resapi-resutilenumproperties">ResUtilEnumProperties</a>
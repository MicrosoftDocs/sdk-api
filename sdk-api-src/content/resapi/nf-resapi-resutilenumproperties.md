---
UID: NF:resapi.ResUtilEnumProperties
title: ResUtilEnumProperties function (resapi.h)
description: Enumerates the property names of a cluster object. The PRESUTIL_ENUM_PROPERTIES type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_ENUM_PROPERTIES","PRESUTIL_ENUM_PROPERTIES function [Failover Cluster]","ResUtilEnumProperties","ResUtilEnumProperties function [Failover Cluster]","_wolf_resutilenumproperties","mscs.resutilenumproperties","resapi/PRESUTIL_ENUM_PROPERTIES","resapi/ResUtilEnumProperties"]
old-location: mscs\resutilenumproperties.htm
tech.root: MsCS
ms.assetid: 1b3a6326-c0da-470a-9cd5-19daa9d48ccd
ms.date: 12/05/2018
ms.keywords: PRESUTIL_ENUM_PROPERTIES, PRESUTIL_ENUM_PROPERTIES function [Failover Cluster], ResUtilEnumProperties, ResUtilEnumProperties function [Failover Cluster], _wolf_resutilenumproperties, mscs.resutilenumproperties, resapi/PRESUTIL_ENUM_PROPERTIES, resapi/ResUtilEnumProperties
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
 - ResUtilEnumProperties
 - resapi/ResUtilEnumProperties
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
 - ResUtilEnumProperties
---

# ResUtilEnumProperties function


## -description

Enumerates the property names of a  <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster object</a>. The <b>PRESUTIL_ENUM_PROPERTIES</b> type defines a pointer to this function.

## -parameters

### -param pPropertyTable [in]

Pointer to an array of  <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a> structures describing properties to enumerate.

### -param pszOutProperties [out]

Pointer to the output buffer in which to return the names of all of the properties in multiple string format. Each property name is stored as a null-terminated Unicode string. The last property name is followed by a final null-terminating character.

### -param cbOutPropertiesSize [in]

Size in bytes of the output buffer pointed to by <i>pszOutProperties</i>.

### -param pcbBytesReturned [out]

Pointer to the total number of bytes in the property list pointed to by <i>pszOutProperties</i>.

### -param pcbRequired [out]

Number of bytes required if the output buffer is too small.

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

<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a>
---
UID: NF:resapi.ResUtilGetAllProperties
title: ResUtilGetAllProperties function (resapi.h)
description: Returns a property list that includes all of the default and unknown properties for a cluster object. The PRESUTIL_GET_ALL_PROPERTIES type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_ALL_PROPERTIES","PRESUTIL_GET_ALL_PROPERTIES function [Failover Cluster]","ResUtilGetAllProperties","ResUtilGetAllProperties function [Failover Cluster]","_wolf_resutilgetallproperties","mscs.resutilgetallproperties","resapi/PRESUTIL_GET_ALL_PROPERTIES","resapi/ResUtilGetAllProperties"]
old-location: mscs\resutilgetallproperties.htm
tech.root: MsCS
ms.assetid: 18a27e1c-e709-4b0a-97c1-b0697deb8dc7
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_ALL_PROPERTIES, PRESUTIL_GET_ALL_PROPERTIES function [Failover Cluster], ResUtilGetAllProperties, ResUtilGetAllProperties function [Failover Cluster], _wolf_resutilgetallproperties, mscs.resutilgetallproperties, resapi/PRESUTIL_GET_ALL_PROPERTIES, resapi/ResUtilGetAllProperties
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
 - ResUtilGetAllProperties
 - resapi/ResUtilGetAllProperties
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
 - ResUtilGetAllProperties
---

# ResUtilGetAllProperties function


## -description

Returns a  <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a> that includes all of the default and  <a href="/previous-versions/windows/desktop/mscs/unknown-properties">unknown</a> properties for a  <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster object</a>. The <b>PRESUTIL_GET_ALL_PROPERTIES</b> type defines a pointer to this function.

## -parameters

### -param hkeyClusterKey [in]

Pointer to the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key that identifies the location of the properties to retrieve.

### -param pPropertyTable [in]

Pointer to an array of  <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a> structures that describe the properties to retrieve.

### -param pOutPropertyList [out]

Pointer to an output buffer in which to return the property list.

### -param cbOutPropertyListSize [in]

Size in bytes of the output buffer pointed to by <i>OutBuffer</i>.

### -param pcbBytesReturned [out]

Pointer to the total number of bytes in the property list pointed to by <i>OutBuffer</i>.

### -param pcbRequired [out]

Pointer to the number of bytes that is required if <i>OutBuffer</i> is too small.

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

## -remarks

The  <b>ResUtilGetAllProperties</b> utility function makes an entry in the property list for each property that is:

<ul>
<li>Included in the  <a href="/previous-versions/windows/desktop/mscs/property-tables">property table</a>.</li>
<li>Included in the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> below the key identified by the <i>ClusterKey</i> parameter, regardless of whether the property is included in the property table.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a>
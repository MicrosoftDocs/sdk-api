---
UID: NF:resapi.ResUtilGetProperties
title: ResUtilGetProperties function (resapi.h)
description: Retrieves properties specified by a property table from the cluster database and returns them in a property list. The PRESUTIL_GET_PROPERTIES type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_PROPERTIES","PRESUTIL_GET_PROPERTIES function [Failover Cluster]","ResUtilGetProperties","ResUtilGetProperties function [Failover Cluster]","_wolf_resutilgetproperties","mscs.resutilgetproperties","resapi/PRESUTIL_GET_PROPERTIES","resapi/ResUtilGetProperties"]
old-location: mscs\resutilgetproperties.htm
tech.root: MsCS
ms.assetid: 6ed03916-660f-4862-b638-900c9b8e4bef
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_PROPERTIES, PRESUTIL_GET_PROPERTIES function [Failover Cluster], ResUtilGetProperties, ResUtilGetProperties function [Failover Cluster], _wolf_resutilgetproperties, mscs.resutilgetproperties, resapi/PRESUTIL_GET_PROPERTIES, resapi/ResUtilGetProperties
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
 - ResUtilGetProperties
 - resapi/ResUtilGetProperties
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
 - ResUtilGetProperties
---

# ResUtilGetProperties function


## -description

Retrieves properties specified by a  <a href="/previous-versions/windows/desktop/mscs/property-tables">property table</a> from 
    the <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> and returns them in a 
    <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a>. The 
    <b>PRESUTIL_GET_PROPERTIES</b> type defines a pointer to this function.

## -parameters

### -param hkeyClusterKey [in]

Pointer to the cluster database key that identifies the location of the properties to retrieve.

### -param pPropertyTable [in]

Pointer to an array of  <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a> structures that describe the properties to retrieve.

### -param pOutPropertyList [out]

Pointer to an output buffer in which to return the property list.

### -param cbOutPropertyListSize [in]

Size in bytes of the output buffer pointed to by <i>pOutPropertyList</i>.

### -param pcbBytesReturned [out]

Pointer to the total number of bytes in the property list pointed to by <i>pOutPropertyList</i>.

### -param pcbRequired [out]

Pointer to the number of bytes that is required if <i>pOutPropertyList</i> is too small.

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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The output buffer was too small to contain the resulting data. The <i>pcbRequired</i> parameter indicates the required size.

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
</table>

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetprivateproperties">ResUtilGetPrivateProperties</a>
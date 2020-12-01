---
UID: NF:resapi.ResUtilGetProperty
title: ResUtilGetProperty function (resapi.h)
description: Returns a specified property from the cluster database. The PRESUTIL_GET_PROPERTY type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_PROPERTY","PRESUTIL_GET_PROPERTY function [Failover Cluster]","ResUtilGetProperty","ResUtilGetProperty function [Failover Cluster]","_wolf_resutilgetproperty","mscs.resutilgetproperty","resapi/PRESUTIL_GET_PROPERTY","resapi/ResUtilGetProperty"]
old-location: mscs\resutilgetproperty.htm
tech.root: MsCS
ms.assetid: f1c6f69c-fc64-4e64-9543-449fc8780eef
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_PROPERTY, PRESUTIL_GET_PROPERTY function [Failover Cluster], ResUtilGetProperty, ResUtilGetProperty function [Failover Cluster], _wolf_resutilgetproperty, mscs.resutilgetproperty, resapi/PRESUTIL_GET_PROPERTY, resapi/ResUtilGetProperty
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
 - ResUtilGetProperty
 - resapi/ResUtilGetProperty
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
 - ResUtilGetProperty
---

# ResUtilGetProperty function


## -description

Returns a specified property from the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>. The <b>PRESUTIL_GET_PROPERTY</b> type defines a pointer to this function.

## -parameters

### -param hkeyClusterKey [in]

Pointer to the cluster database key identifying the location of the property to retrieve.

### -param pPropertyTableItem [in]

Pointer to a  <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a> structure that describes the property to retrieve.

### -param pOutPropertyItem [out]

Pointer to an output buffer in which to return the requested property. It is assumed that the buffer is part of a  <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a>.

### -param pcbOutPropertyItemSize [in, out]

Pointer to the size in bytes of the output buffer pointed to by <i>pOutPropertyItem</i>.

## -returns

If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following is a possible error code.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a>
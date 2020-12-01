---
UID: NF:resapi.ResUtilGetPropertySize
title: ResUtilGetPropertySize function (resapi.h)
description: Returns the total number of bytes required for a specified property.
helpviewer_keywords: ["PRESUTIL_GET_PROPERTY_SIZE","PRESUTIL_GET_PROPERTY_SIZE function [Failover Cluster]","ResUtilGetPropertySize","ResUtilGetPropertySize function [Failover Cluster]","_wolf_resutilgetpropertysize","mscs.resutilgetpropertysize","resapi/PRESUTIL_GET_PROPERTY_SIZE","resapi/ResUtilGetPropertySize"]
old-location: mscs\resutilgetpropertysize.htm
tech.root: MsCS
ms.assetid: 0f21ef2b-747c-4fb3-a13c-16bcb7bfd46e
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_PROPERTY_SIZE, PRESUTIL_GET_PROPERTY_SIZE function [Failover Cluster], ResUtilGetPropertySize, ResUtilGetPropertySize function [Failover Cluster], _wolf_resutilgetpropertysize, mscs.resutilgetpropertysize, resapi/PRESUTIL_GET_PROPERTY_SIZE, resapi/ResUtilGetPropertySize
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
 - ResUtilGetPropertySize
 - resapi/ResUtilGetPropertySize
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
 - ResUtilGetPropertySize
---

# ResUtilGetPropertySize function


## -description

Returns the total number of bytes required for a specified property.

## -parameters

### -param hkeyClusterKey [in]

<a href="/previous-versions/windows/desktop/mscs/cluster-database">Cluster database</a> key identifying the location of the property to size.

### -param pPropertyTableItem [in]

Pointer to a  <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a> structure describing the property to size.

### -param pcbOutPropertyListSize [in, out]

Pointer to the total number of bytes required for the property value, which includes the  <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure and the data.

### -param pnPropertyCount [in, out]

Pointer to the total number of properties. This value is incremented to include this property if  <b>ResUtilGetPropertySize</b> is successful.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The data type of a property specified in the property table does not match the data type of the same-named property stored in the cluster database.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a>



<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a>
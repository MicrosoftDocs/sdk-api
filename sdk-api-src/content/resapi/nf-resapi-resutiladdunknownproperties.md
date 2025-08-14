---
UID: NF:resapi.ResUtilAddUnknownProperties
title: ResUtilAddUnknownProperties function (resapi.h)
description: Retrieves a set of unknown properties from the cluster database and appends them to the end of a property list.
helpviewer_keywords: ["PRESUTIL_ADD_UNKNOWN_PROPERTIES","PRESUTIL_ADD_UNKNOWN_PROPERTIES function [Failover Cluster]","ResUtilAddUnknownProperties","ResUtilAddUnknownProperties function [Failover Cluster]","_wolf_resutiladdunknownproperties","mscs.resutiladdunknownproperties","resapi/PRESUTIL_ADD_UNKNOWN_PROPERTIES","resapi/ResUtilAddUnknownProperties"]
old-location: mscs\resutiladdunknownproperties.htm
tech.root: MsCS
ms.assetid: 17659c86-d7cc-4316-ba0e-ce71de727fa1
ms.date: 12/05/2018
ms.keywords: PRESUTIL_ADD_UNKNOWN_PROPERTIES, PRESUTIL_ADD_UNKNOWN_PROPERTIES function [Failover Cluster], ResUtilAddUnknownProperties, ResUtilAddUnknownProperties function [Failover Cluster], _wolf_resutiladdunknownproperties, mscs.resutiladdunknownproperties, resapi/PRESUTIL_ADD_UNKNOWN_PROPERTIES, resapi/ResUtilAddUnknownProperties
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
 - ResUtilAddUnknownProperties
 - resapi/ResUtilAddUnknownProperties
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
 - ResUtilAddUnknownProperties
---

# ResUtilAddUnknownProperties function


## -description

Retrieves a set of  <a href="/previous-versions/windows/desktop/mscs/unknown-properties">unknown properties</a> from the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> and appends them to the end of a  <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a>.

## -parameters

### -param hkeyClusterKey [in]

Pointer to the cluster database key that identifies the location for the properties to read.

### -param pPropertyTable [in]

Pointer to a  <a href="/previous-versions/windows/desktop/mscs/property-tables">property table</a> describing the common and private properties of an object. Any properties found in the cluster database that are not in this property table are added to the property list.

### -param pOutPropertyList [in, out]

Pointer to a buffer in which to receive the returned properties. On input, the buffer can contain an existing property list, or it can be empty. On output, the retrieved properties will be appended to the end of the existing list, or, if the buffer is empty, will return as a new property list.

### -param pcbOutPropertyListSize [in]

Total byte size of the buffer pointed to by <i>pOutPropertyList</i>. The size of the buffer must be large enough to contain the existing property list and the property list to be returned.

### -param pcbBytesReturned [in, out]

On input, pointer to the byte size of the property list contained by the pOutPropertyList buffer. On output, pointer to the total number of bytes in the property list pointed to by <i>pOutPropertyList</i>.

### -param pcbRequired [in, out]

On output, points to the total number of bytes required to hold the returned property list. If the <i>pOutPropertyList</i> buffer was too small, it can be reallocated to the required size.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was an error allocating memory.

</td>
</tr>
</table>

## -remarks

The relationships between the input and output parameters of  <b>ResUtilAddUnknownProperties</b> are illustrated in the following diagram:

:::image type="content" source="./images/resutil.png" border="false" alt-text="Diagram showing input and output parameters listed separately in two buffers. Two unknown properties have been added to the output parameter list.":::

The  <b>ResUtilAddUnknownProperties</b> utility function enumerates the properties stored in the cluster database (under <i>hkeyClusterKey</i>) and looks for corresponding properties in the property table (<i>pPropertyTable</i>). Each property that is listed in the cluster database but not listed in the property table is added to the property list (<i>pOutPropertyList</i>).

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetunknownproperties">ResUtilSetUnknownProperties</a>
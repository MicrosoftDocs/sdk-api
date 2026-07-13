---
UID: NF:resapi.ResUtilVerifyPropertyTable
title: ResUtilVerifyPropertyTable function (resapi.h)
description: Uses a property table to verify that a property list is correctly formatted.
helpviewer_keywords: ["PRESUTIL_VERIFY_PROPERTY_TABLE","PRESUTIL_VERIFY_PROPERTY_TABLE function [Failover Cluster]","ResUtilVerifyPropertyTable","ResUtilVerifyPropertyTable function [Failover Cluster]","_wolf_resutilverifypropertytable","mscs.resutilverifypropertytable","resapi/PRESUTIL_VERIFY_PROPERTY_TABLE","resapi/ResUtilVerifyPropertyTable"]
old-location: mscs\resutilverifypropertytable.htm
tech.root: MsCS
ms.assetid: 5a079081-c11a-4f85-89d4-09a5e7fab29f
ms.date: 12/05/2018
ms.keywords: PRESUTIL_VERIFY_PROPERTY_TABLE, PRESUTIL_VERIFY_PROPERTY_TABLE function [Failover Cluster], ResUtilVerifyPropertyTable, ResUtilVerifyPropertyTable function [Failover Cluster], _wolf_resutilverifypropertytable, mscs.resutilverifypropertytable, resapi/PRESUTIL_VERIFY_PROPERTY_TABLE, resapi/ResUtilVerifyPropertyTable
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
 - ResUtilVerifyPropertyTable
 - resapi/ResUtilVerifyPropertyTable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-resutils-l1-1-3.dll
 - ext-ms-win-cluster-resutils-l1-1-2.dll
 - ResUtils.dll
 - Ext-MS-Win-Cluster-ResUtils-L1-1-1.dll
api_name:
 - ResUtilVerifyPropertyTable
---

# ResUtilVerifyPropertyTable function


## -description

Uses a  <a href="/previous-versions/windows/desktop/mscs/property-tables">property table</a> to verify that a <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a> is correctly formatted.

## -parameters

### -param pPropertyTable [in]

Pointer to a property table describing the properties that will be validated in the property list.

### -param Reserved

This parameter is reserved for future use.

### -param bAllowUnknownProperties [in]

If <b>TRUE</b>, the function ignores all properties in the property list that are not included in the property table. If <b>FALSE</b>, any property in the property list that is not included in the property table causes the function to return <b>ERROR_INVALID_PARAMETER</b>.

### -param pInPropertyList [in]

Pointer to the input buffer containing the property list to validate.

### -param cbInPropertyListSize [in]

Size in bytes of the input buffer pointed to by <i>pInPropertyList</i>.

### -param pOutParams [out, optional]

Pointer to a parameter block.

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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The property list buffer is larger than reported by the <i>cbInPropertyListSize</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
No property list buffer was specified, or the property list is formatted incorrectly

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The property list is formatted incorrectly. If <i>bAllowUnknownProperties</i> is set to <b>FALSE</b>, the property list may contain properties that are not present in the property table.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a>
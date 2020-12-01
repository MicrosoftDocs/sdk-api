---
UID: NF:resapi.ResUtilGetMultiSzProperty
title: ResUtilGetMultiSzProperty function (resapi.h)
description: Retrieves a multiple string property from a property list and advances a pointer to the next property in the list. The PRESUTIL_GET_MULTI_SZ_PROPERTY type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_MULTI_SZ_PROPERTY","PRESUTIL_GET_MULTI_SZ_PROPERTY function [Failover Cluster]","ResUtilGetMultiSzProperty","ResUtilGetMultiSzProperty function [Failover Cluster]","_wolf_resutilgetmultiszproperty","mscs.resutilgetmultiszproperty","resapi/PRESUTIL_GET_MULTI_SZ_PROPERTY","resapi/ResUtilGetMultiSzProperty"]
old-location: mscs\resutilgetmultiszproperty.htm
tech.root: MsCS
ms.assetid: 7f345cce-fa67-467c-bd4f-286609c3f757
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_MULTI_SZ_PROPERTY, PRESUTIL_GET_MULTI_SZ_PROPERTY function [Failover Cluster], ResUtilGetMultiSzProperty, ResUtilGetMultiSzProperty function [Failover Cluster], _wolf_resutilgetmultiszproperty, mscs.resutilgetmultiszproperty, resapi/PRESUTIL_GET_MULTI_SZ_PROPERTY, resapi/ResUtilGetMultiSzProperty
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
 - ResUtilGetMultiSzProperty
 - resapi/ResUtilGetMultiSzProperty
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
 - ResUtilGetMultiSzProperty
---

# ResUtilGetMultiSzProperty function


## -description

Retrieves a multiple string 
    property from a <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a> and advances a pointer to the 
    next property in the list. The <b>PRESUTIL_GET_MULTI_SZ_PROPERTY</b> type defines a pointer to this function.

## -parameters

### -param ppszOutValue [out]

Address of a pointer in which the multiple string value from the property list will be returned.

### -param pcbOutValueSize [out]

Pointer to the size of the output value.

### -param pValueStruct [in]

Pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_sz">CLUSPROP_MULTI_SZ</a> structure 
      specifying the multiple string value to retrieve from the property list.

### -param pszOldValue [in, optional]

Pointer to the previous value of the property.

### -param cbOldValueSize [in]

Pointer to the length of the previous value of the property.

### -param ppPropertyList [in, out]

Address of the pointer to the property list buffer containing the multiple string property. This pointer 
      will be advanced to the beginning of the next property.

### -param pcbPropertyListSize [in, out]

Pointer to the size of the property list buffer. The size will be decremented to account for the advance of 
      the <i>ppPropertyList</i> pointer.

## -returns

If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
      <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following is a possible error 
      code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The data is formatted incorrectly.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetbinaryproperty">ResUtilGetBinaryProperty</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetdwordproperty">ResUtilGetDwordProperty</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetszproperty">ResUtilGetSzProperty</a>
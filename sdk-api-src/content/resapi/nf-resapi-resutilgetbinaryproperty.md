---
UID: NF:resapi.ResUtilGetBinaryProperty
title: ResUtilGetBinaryProperty function (resapi.h)
description: Retrieves a binary property from a property list and advances a pointer to the next property in the list. The PRESUTIL_GET_BINARY_PROPERTY type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_BINARY_PROPERTY","PRESUTIL_GET_BINARY_PROPERTY function [Failover Cluster]","ResUtilGetBinaryProperty","ResUtilGetBinaryProperty function [Failover Cluster]","_wolf_resutilgetbinaryproperty","mscs.resutilgetbinaryproperty","resapi/PRESUTIL_GET_BINARY_PROPERTY","resapi/ResUtilGetBinaryProperty"]
old-location: mscs\resutilgetbinaryproperty.htm
tech.root: MsCS
ms.assetid: fe69ba4c-d69a-4f5a-a620-0e2152e7be61
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_BINARY_PROPERTY, PRESUTIL_GET_BINARY_PROPERTY function [Failover Cluster], ResUtilGetBinaryProperty, ResUtilGetBinaryProperty function [Failover Cluster], _wolf_resutilgetbinaryproperty, mscs.resutilgetbinaryproperty, resapi/PRESUTIL_GET_BINARY_PROPERTY, resapi/ResUtilGetBinaryProperty
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
 - ResUtilGetBinaryProperty
 - resapi/ResUtilGetBinaryProperty
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
 - ResUtilGetBinaryProperty
---

# ResUtilGetBinaryProperty function


## -description

Retrieves a binary property from 
    a <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a> and advances a pointer to the next property 
    in the list. The <b>PRESUTIL_GET_BINARY_PROPERTY</b> type defines a pointer to this function.

## -parameters

### -param ppbOutValue [out]

Address of a pointer in which the binary value from the property list will be returned.

### -param pcbOutValueSize [out]

Pointer to the size of the output value.

### -param pValueStruct [in]

Pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_binary">CLUSPROP_BINARY</a> structure specifying 
      the binary value to retrieve from the property list.

### -param pbOldValue [in, optional]

Pointer to the previous value of the property.

### -param cbOldValueSize [in]

Pointer to the length of the previous value of the property.

### -param ppPropertyList [in, out]

Address of the pointer to the property list buffer containing the binary property. This pointer will be 
      advanced to the beginning of the next property.

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

<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetdwordproperty">ResUtilGetDwordProperty</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetmultiszproperty">ResUtilGetMultiSzProperty</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetszproperty">ResUtilGetSzProperty</a>
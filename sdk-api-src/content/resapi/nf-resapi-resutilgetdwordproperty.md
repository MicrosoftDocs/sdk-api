---
UID: NF:resapi.ResUtilGetDwordProperty
title: ResUtilGetDwordProperty function (resapi.h)
description: Retrieves a DWORD property from a property list and advances a pointer to the next property in the list. The PRESUTIL_GET_DWORD_PROPERTY type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_DWORD_PROPERTY","PRESUTIL_GET_DWORD_PROPERTY function [Failover Cluster]","ResUtilGetDwordProperty","ResUtilGetDwordProperty function [Failover Cluster]","_wolf_resutilgetdwordproperty","mscs.resutilgetdwordproperty","resapi/PRESUTIL_GET_DWORD_PROPERTY","resapi/ResUtilGetDwordProperty"]
old-location: mscs\resutilgetdwordproperty.htm
tech.root: MsCS
ms.assetid: d67f73f8-a5ce-4922-956f-392c27ee3b1d
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_DWORD_PROPERTY, PRESUTIL_GET_DWORD_PROPERTY function [Failover Cluster], ResUtilGetDwordProperty, ResUtilGetDwordProperty function [Failover Cluster], _wolf_resutilgetdwordproperty, mscs.resutilgetdwordproperty, resapi/PRESUTIL_GET_DWORD_PROPERTY, resapi/ResUtilGetDwordProperty
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
 - ResUtilGetDwordProperty
 - resapi/ResUtilGetDwordProperty
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
 - ResUtilGetDwordProperty
---

# ResUtilGetDwordProperty function


## -description

Retrieves a 
    <b>DWORD</b> property from a 
    <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a> and advances a pointer to the next property in 
    the list. The <b>PRESUTIL_GET_DWORD_PROPERTY</b> type defines a pointer to this function.

## -parameters

### -param pdwOutValue [out]

Address of a pointer in which the <b>DWORD</b> value from the property list will be 
      returned.

### -param pValueStruct [in]

Pointer to a <a href="/previous-versions/windows/desktop/legacy/aa368375(v=vs.85)">CLUSPROP_DWORD</a> structure specifying 
      the <b>DWORD</b> value to retrieve from the property list.

### -param dwOldValue [in]

Specifies the previous value of the property.

### -param dwMinimum [in]

Specifies the minimum value allowed for the property.

### -param dwMaximum [in]

Specifies the maximum value allowed for the property.

### -param ppPropertyList [out]

Address of the pointer to the property list buffer containing the <b>DWORD</b> 
      property. This pointer will be advanced to the beginning of the next property.

### -param pcbPropertyListSize [out]

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

## -remarks

The <b>ResUtilGetDwordProperty</b> utility function verifies that the value returned 
    in <i>pdwOutValue</i> is within the range specified by <i>dwMinimum</i> and 
    <i>dwMaximum</i>. If <i>dwMinimum</i> and 
    <i>dwMaximum</i> are both set to 0, no range checking is done.

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetbinaryproperty">ResUtilGetBinaryProperty</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetmultiszproperty">ResUtilGetMultiSzProperty</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetszproperty">ResUtilGetSzProperty</a>
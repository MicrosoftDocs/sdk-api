---
UID: NF:resapi.ResUtilFindLongProperty
title: ResUtilFindLongProperty function (resapi.h)
description: Locates a signed long property value in a property list. The PRESUTIL_FIND_LONG_PROPERTY type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_FIND_LONG_PROPERTY","PRESUTIL_FIND_LONG_PROPERTY function [Failover Cluster]","ResUtilFindLongProperty","ResUtilFindLongProperty function [Failover Cluster]","_wolf_resutilfindlongproperty","mscs.resutilfindlongproperty","resapi/PRESUTIL_FIND_LONG_PROPERTY","resapi/ResUtilFindLongProperty"]
old-location: mscs\resutilfindlongproperty.htm
tech.root: MsCS
ms.assetid: 6f75be85-37ef-4e2b-a588-bc1238cd8760
ms.date: 12/05/2018
ms.keywords: PRESUTIL_FIND_LONG_PROPERTY, PRESUTIL_FIND_LONG_PROPERTY function [Failover Cluster], ResUtilFindLongProperty, ResUtilFindLongProperty function [Failover Cluster], _wolf_resutilfindlongproperty, mscs.resutilfindlongproperty, resapi/PRESUTIL_FIND_LONG_PROPERTY, resapi/ResUtilFindLongProperty
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
 - ResUtilFindLongProperty
 - resapi/ResUtilFindLongProperty
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
 - ResUtilFindLongProperty
---

# ResUtilFindLongProperty function


## -description

Locates a signed long property value in a  <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a>. The <b>PRESUTIL_FIND_LONG_PROPERTY</b> type defines a pointer to this function.

## -parameters

### -param pPropertyList [in]

Pointer to the property list in which to locate the value.

### -param cbPropertyListSize [in]

Size in bytes of the data included in <i>pPropertyList</i>.

### -param pszPropertyName [in]

Pointer to a null-terminated Unicode string containing the name of the value to locate.

### -param plPropertyValue [out]

Pointer to the actual value of the data stored in the property list buffer.

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
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The data is in an incorrect format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The property could not be located in the property list.

</td>
</tr>
</table>

## -remarks

If the operation is successful, <i>plPropertyValue</i> points directly into the property list buffer. Be careful not to disturb the formatting of the property list when using <i>plPropertyValue</i>.

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutilfindbinaryproperty">ResUtilFindBinaryProperty</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilfinddwordproperty">ResUtilFindDwordProperty</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilfindexpandszproperty">ResUtilFindExpandSzProperty</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilfindexpandedszproperty">ResUtilFindExpandedSzProperty</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilfindmultiszproperty">ResUtilFindMultiSzProperty</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilfindszproperty">ResUtilFindSzProperty</a>
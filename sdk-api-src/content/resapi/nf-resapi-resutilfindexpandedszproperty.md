---
UID: NF:resapi.ResUtilFindExpandedSzProperty
title: ResUtilFindExpandedSzProperty function (resapi.h)
description: Locates an expanded string property value in a property list. The PRESUTIL_FIND_EXPANDED_SZ_PROPERTY type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_FIND_EXPANDED_SZ_PROPERTY","PRESUTIL_FIND_EXPANDED_SZ_PROPERTY function [Failover Cluster]","ResUtilFindExpandedSzProperty","ResUtilFindExpandedSzProperty function [Failover Cluster]","_wolf_resutilfindexpandedszproperty","mscs.resutilfindexpandedszproperty","resapi/PRESUTIL_FIND_EXPANDED_SZ_PROPERTY","resapi/ResUtilFindExpandedSzProperty"]
old-location: mscs\resutilfindexpandedszproperty.htm
tech.root: MsCS
ms.assetid: 7a639932-6dd5-41ef-a126-c2d5001a436f
ms.date: 12/05/2018
ms.keywords: PRESUTIL_FIND_EXPANDED_SZ_PROPERTY, PRESUTIL_FIND_EXPANDED_SZ_PROPERTY function [Failover Cluster], ResUtilFindExpandedSzProperty, ResUtilFindExpandedSzProperty function [Failover Cluster], _wolf_resutilfindexpandedszproperty, mscs.resutilfindexpandedszproperty, resapi/PRESUTIL_FIND_EXPANDED_SZ_PROPERTY, resapi/ResUtilFindExpandedSzProperty
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
 - ResUtilFindExpandedSzProperty
 - resapi/ResUtilFindExpandedSzProperty
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
 - ResUtilFindExpandedSzProperty
---

# ResUtilFindExpandedSzProperty function


## -description

Locates an expanded string property value in a  <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a>. The <b>PRESUTIL_FIND_EXPANDED_SZ_PROPERTY</b> type defines a pointer to this function.

## -parameters

### -param pPropertyList [in]

Pointer to the property list in which to locate the value.

### -param cbPropertyListSize [in]

Size in bytes of the data included in <i>pPropertyList</i>.

### -param pszPropertyName [in]

Pointer to a null-terminated Unicode string containing the name of the value to locate.

### -param pszPropertyValue [out, optional]

Pointer to a <b>WCHAR</b> pointer to a buffer (allocated by the function) containing a copy of the property value. You must call <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> (on *<i>pszPropertyValue</i>) to free the allocated memory. If no value is required, pass <b>NULL</b> for this parameter.

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
The property list is incorrectly formatted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function could not allocate a buffer in which to return the property value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified property could not be located in the property list.

</td>
</tr>
</table>

## -remarks

If  <a href="/windows/desktop/api/resapi/nf-resapi-resutilfindexpandszproperty">ResUtilFindExpandSzProperty</a> is successful, *<i>pszPropertyValue</i> points to a copy of the data stored in <i>pPropertyList</i>. Be sure to call <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> on *<i>pszPropertyValue</i> to prevent memory leaks.

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutilfindbinaryproperty">ResUtilFindBinaryProperty</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilfinddwordproperty">ResUtilFindDwordProperty</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilfindexpandszproperty">ResUtilFindExpandSzProperty</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilfindlongproperty">ResUtilFindLongProperty</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilfindmultiszproperty">ResUtilFindMultiSzProperty</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilfindszproperty">ResUtilFindSzProperty</a>
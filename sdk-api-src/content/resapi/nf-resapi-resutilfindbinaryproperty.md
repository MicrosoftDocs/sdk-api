---
UID: NF:resapi.ResUtilFindBinaryProperty
title: ResUtilFindBinaryProperty function (resapi.h)
description: Locates a specified binary property in a property list and can also return the value of the property. The PRESUTIL_FIND_BINARY_PROPERTY type defines a pointer to this function.helpviewer_keywords: ["PRESUTIL_FIND_BINARY_PROPERTY","PRESUTIL_FIND_BINARY_PROPERTY function [Failover Cluster]","ResUtilFindBinaryProperty","ResUtilFindBinaryProperty function [Failover Cluster]","_wolf_resutilfindbinaryproperty","mscs.resutilfindbinaryproperty","resapi/PRESUTIL_FIND_BINARY_PROPERTY","resapi/ResUtilFindBinaryProperty"]
old-location: mscs\resutilfindbinaryproperty.htm
tech.root: MsCS
ms.assetid: 3be864ae-dc02-47e7-aa86-a6c14be13091
ms.date: 12/05/2018
ms.keywords: PRESUTIL_FIND_BINARY_PROPERTY, PRESUTIL_FIND_BINARY_PROPERTY function [Failover Cluster], ResUtilFindBinaryProperty, ResUtilFindBinaryProperty function [Failover Cluster], _wolf_resutilfindbinaryproperty, mscs.resutilfindbinaryproperty, resapi/PRESUTIL_FIND_BINARY_PROPERTY, resapi/ResUtilFindBinaryProperty
f1_keywords:
- resapi/ResUtilFindBinaryProperty
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ResUtils.dll
api_name:
- ResUtilFindBinaryProperty
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ResUtilFindBinaryProperty function


## -description


Locates a specified binary property in a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/property-lists">property list</a> and can also return the value of the property. The <b>PRESUTIL_FIND_BINARY_PROPERTY</b> type defines a pointer to this function.


## -parameters




### -param pPropertyList [in]

Pointer to the property list in which to locate the value.


### -param cbPropertyListSize [in]

Size, in bytes, of the property list specified by <i>pPropertyList</i>.


### -param pszPropertyName [in]

Pointer to a null-terminated Unicode string containing the name of the property to locate.


### -param pbPropertyValue [out, optional]

Pointer to a <b>BYTE</b> pointer to a buffer (allocated by the function) containing a copy of the property value. You must call <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> (on *<i>pbPropertyValue</i>) to free the allocated memory. If no value is required, pass <b>NULL</b> for this parameter.


### -param pcbPropertyValueSize [out, optional]

Pointer to the size, in bytes, of the value returned. If no size is required, pass <b>NULL</b> for this parameter.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>. The following are possible error codes.

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



If  <b>ResUtilFindBinaryProperty</b> is successful, *<i>pbPropertyValue</i> points to a copy of the data stored in <i>pPropertyList</i>. Be sure to call <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> on *<i>pbPropertyValue</i> to prevent memory leaks.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nf-resapi-resutilfinddwordproperty">ResUtilFindDwordProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nf-resapi-resutilfindexpandszproperty">ResUtilFindExpandSzProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nf-resapi-resutilfindexpandedszproperty">ResUtilFindExpandedSzProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nf-resapi-resutilfindlongproperty">ResUtilFindLongProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nf-resapi-resutilfindmultiszproperty">ResUtilFindMultiSzProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/resapi/nf-resapi-resutilfindszproperty">ResUtilFindSzProperty</a>
 

 


---
UID: NF:resapi.ResUtilGetSzProperty
title: ResUtilGetSzProperty function
author: windows-sdk-content
description: Retrieves a string property from a property list and advances a pointer to the next property in the list. The PRESUTIL_GET_SZ_PROPERTY type defines a pointer to this function.
old-location: mscs\resutilgetszproperty.htm
tech.root: mscs
ms.assetid: 0f485910-e691-48fa-a96b-79573ce60616
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PRESUTIL_GET_SZ_PROPERTY, PRESUTIL_GET_SZ_PROPERTY function [Failover Cluster], ResUtilGetSzProperty, ResUtilGetSzProperty function [Failover Cluster], _wolf_resutilgetszproperty, mscs.resutilgetszproperty, resapi/PRESUTIL_GET_SZ_PROPERTY, resapi/ResUtilGetSzProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - ResUtilGetSzProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilGetSzProperty function


## -description


Retrieves a string property from a 
    <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a> and advances a pointer to the next property in 
    the list. The <b>PRESUTIL_GET_SZ_PROPERTY</b> type defines a pointer to this function.


## -parameters




### -param ppszOutValue [out]

Address of a pointer in which the string value from the property list will be returned.


### -param pValueStruct [in]

Pointer to a <a href="https://msdn.microsoft.com/f991ac6f-5272-44ee-a035-c9501bf7d866">CLUSPROP_SZ</a> structure specifying the 
      string value to retrieve from the property list.


### -param pszOldValue [in, optional]

Pointer to the previous value of the property.


### -param ppPropertyList [in, out]

Address of the pointer to the property list buffer containing the string property. This pointer will be 
      advanced to the beginning of the next property.


### -param pcbPropertyListSize [in, out]

Pointer to the size of the property list buffer. The size will be decremented to account for the advance of 
      the <i>ppPropertyList</i> pointer.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error 
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




<a href="https://msdn.microsoft.com/fe69ba4c-d69a-4f5a-a620-0e2152e7be61">ResUtilGetBinaryProperty</a>



<a href="https://msdn.microsoft.com/d67f73f8-a5ce-4922-956f-392c27ee3b1d">ResUtilGetDwordProperty</a>



<a href="https://msdn.microsoft.com/7f345cce-fa67-467c-bd4f-286609c3f757">ResUtilGetMultiSzProperty</a>
 

 


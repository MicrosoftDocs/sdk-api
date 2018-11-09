---
UID: NF:resapi.ResUtilGetDwordProperty
title: ResUtilGetDwordProperty function
author: windows-sdk-content
description: Retrieves a DWORD property from a property list and advances a pointer to the next property in the list. The PRESUTIL_GET_DWORD_PROPERTY type defines a pointer to this function.
old-location: mscs\resutilgetdwordproperty.htm
tech.root: mscs
ms.assetid: d67f73f8-a5ce-4922-956f-392c27ee3b1d
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: PRESUTIL_GET_DWORD_PROPERTY, PRESUTIL_GET_DWORD_PROPERTY function [Failover Cluster], ResUtilGetDwordProperty, ResUtilGetDwordProperty function [Failover Cluster], _wolf_resutilgetdwordproperty, mscs.resutilgetdwordproperty, resapi/PRESUTIL_GET_DWORD_PROPERTY, resapi/ResUtilGetDwordProperty
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
 - ResUtilGetDwordProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilGetDwordProperty function


## -description


Retrieves a 
    <b>DWORD</b> property from a 
    <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a> and advances a pointer to the next property in 
    the list. The <b>PRESUTIL_GET_DWORD_PROPERTY</b> type defines a pointer to this function.


## -parameters




### -param pdwOutValue [out]

Address of a pointer in which the <b>DWORD</b> value from the property list will be 
      returned.


### -param pValueStruct [in]

Pointer to a <a href="https://msdn.microsoft.com/96d81777-be45-4dbb-8426-f68cb51e2a42">CLUSPROP_DWORD</a> structure specifying 
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
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error 
       code.




## -remarks



The <b>ResUtilGetDwordProperty</b> utility function verifies that the value returned 
    in <i>pdwOutValue</i> is within the range specified by <i>dwMinimum</i> and 
    <i>dwMaximum</i>. If <i>dwMinimum</i> and 
    <i>dwMaximum</i> are both set to 0, no range checking is done.




## -see-also




<a href="https://msdn.microsoft.com/fe69ba4c-d69a-4f5a-a620-0e2152e7be61">ResUtilGetBinaryProperty</a>



<a href="https://msdn.microsoft.com/7f345cce-fa67-467c-bd4f-286609c3f757">ResUtilGetMultiSzProperty</a>



<a href="https://msdn.microsoft.com/0f485910-e691-48fa-a96b-79573ce60616">ResUtilGetSzProperty</a>
 

 


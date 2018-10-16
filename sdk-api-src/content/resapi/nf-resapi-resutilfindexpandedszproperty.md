---
UID: NF:resapi.ResUtilFindExpandedSzProperty
title: ResUtilFindExpandedSzProperty function
author: windows-sdk-content
description: Locates an expanded string property value in a property list. The PRESUTIL_FIND_EXPANDED_SZ_PROPERTY type defines a pointer to this function.
old-location: mscs\resutilfindexpandedszproperty.htm
tech.root: mscs
ms.assetid: 7a639932-6dd5-41ef-a126-c2d5001a436f
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: PRESUTIL_FIND_EXPANDED_SZ_PROPERTY, PRESUTIL_FIND_EXPANDED_SZ_PROPERTY function [Failover Cluster], ResUtilFindExpandedSzProperty, ResUtilFindExpandedSzProperty function [Failover Cluster], _wolf_resutilfindexpandedszproperty, mscs.resutilfindexpandedszproperty, resapi/PRESUTIL_FIND_EXPANDED_SZ_PROPERTY, resapi/ResUtilFindExpandedSzProperty
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
 - ResUtilFindExpandedSzProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilFindExpandedSzProperty function


## -description


Locates an expanded string property value in a  <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a>. The <b>PRESUTIL_FIND_EXPANDED_SZ_PROPERTY</b> type defines a pointer to this function.


## -parameters




### -param pPropertyList [in]

Pointer to the property list in which to locate the value.


### -param cbPropertyListSize [in]

Size in bytes of the data included in <i>pPropertyList</i>.


### -param pszPropertyName [in]

Pointer to a null-terminated Unicode string containing the name of the value to locate.


### -param pszPropertyValue [out, optional]

Pointer to a <b>WCHAR</b> pointer to a buffer (allocated by the function) containing a copy of the property value. You must call <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> (on *<i>pszPropertyValue</i>) to free the allocated memory. If no value is required, pass <b>NULL</b> for this parameter.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error codes.




## -remarks



If  <a href="https://msdn.microsoft.com/44fb21bd-6cc2-4b1b-ae8f-c977fa336747">ResUtilFindExpandSzProperty</a> is successful, *<i>pszPropertyValue</i> points to a copy of the data stored in <i>pPropertyList</i>. Be sure to call <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> on *<i>pszPropertyValue</i> to prevent memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/3be864ae-dc02-47e7-aa86-a6c14be13091">ResUtilFindBinaryProperty</a>



<a href="https://msdn.microsoft.com/884e922f-5cc6-4e46-b2f6-2436e7fc634e">ResUtilFindDwordProperty</a>



<a href="https://msdn.microsoft.com/44fb21bd-6cc2-4b1b-ae8f-c977fa336747">ResUtilFindExpandSzProperty</a>



<a href="https://msdn.microsoft.com/6f75be85-37ef-4e2b-a588-bc1238cd8760">ResUtilFindLongProperty</a>



<a href="https://msdn.microsoft.com/65209ca8-e293-40cc-ac8a-9643933e049f">ResUtilFindMultiSzProperty</a>



<a href="https://msdn.microsoft.com/b7fb6c7e-5a13-4838-98f4-45931e9e96d0">ResUtilFindSzProperty</a>
 

 


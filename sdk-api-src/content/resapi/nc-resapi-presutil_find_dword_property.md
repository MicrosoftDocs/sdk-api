---
UID: NC:resapi.PRESUTIL_FIND_DWORD_PROPERTY
title: PRESUTIL_FIND_DWORD_PROPERTY
author: windows-sdk-content
description: Locates an unsigned long property value in a property list. The PRESUTIL_FIND_DWORD_PROPERTY type defines a pointer to this function.
old-location: mscs\resutilfinddwordproperty.htm
old-project: MsCS
ms.assetid: 884e922f-5cc6-4e46-b2f6-2436e7fc634e
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: PRESUTIL_FIND_DWORD_PROPERTY, PRESUTIL_FIND_DWORD_PROPERTY callback, PRESUTIL_FIND_DWORD_PROPERTY callback function [Failover Cluster], _wolf_resutilfinddwordproperty, mscs.resutilfinddwordproperty, resapi/PRESUTIL_FIND_DWORD_PROPERTY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - PRESUTIL_FIND_DWORD_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PRESUTIL_FIND_DWORD_PROPERTY callback function


## -description


Locates an unsigned long property value in a  <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a>. The <b>PRESUTIL_FIND_DWORD_PROPERTY</b> type defines a pointer to this function.


## -parameters




### -param pPropertyList [in]

Pointer to the property list in which to locate the value.


### -param cbPropertyListSize [in]

Size in bytes of the data included in <i>pPropertyList</i>.


### -param pszPropertyName [in]

Pointer to a null-terminated Unicode string containing the name of the value to locate.


### -param pdwPropertyValue [out]

Pointer to the actual value of the data stored in the property list buffer.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error codes.




## -remarks



If the operation is successful, <i>pdwPropertyValue</i> points directly into the property list buffer. Be careful not to disturb the formatting of the property list when using <i>pdwPropertyValue</i>.




## -see-also




<a href="https://msdn.microsoft.com/3be864ae-dc02-47e7-aa86-a6c14be13091">ResUtilFindBinaryProperty</a>



<a href="https://msdn.microsoft.com/44fb21bd-6cc2-4b1b-ae8f-c977fa336747">ResUtilFindExpandSzProperty</a>



<a href="https://msdn.microsoft.com/7a639932-6dd5-41ef-a126-c2d5001a436f">ResUtilFindExpandedSzProperty</a>



<a href="https://msdn.microsoft.com/6f75be85-37ef-4e2b-a588-bc1238cd8760">ResUtilFindLongProperty</a>



<a href="https://msdn.microsoft.com/65209ca8-e293-40cc-ac8a-9643933e049f">ResUtilFindMultiSzProperty</a>



<a href="https://msdn.microsoft.com/b7fb6c7e-5a13-4838-98f4-45931e9e96d0">ResUtilFindSzProperty</a>
 

 


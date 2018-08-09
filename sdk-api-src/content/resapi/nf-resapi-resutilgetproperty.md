---
UID: NF:resapi.ResUtilGetProperty
title: ResUtilGetProperty function
author: windows-sdk-content
description: Returns a specified property from the cluster database. The PRESUTIL_GET_PROPERTY type defines a pointer to this function.
old-location: mscs\resutilgetproperty.htm
old-project: mscs
ms.assetid: f1c6f69c-fc64-4e64-9543-449fc8780eef
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PRESUTIL_GET_PROPERTY, PRESUTIL_GET_PROPERTY function [Failover Cluster], ResUtilGetProperty, ResUtilGetProperty function [Failover Cluster], _wolf_resutilgetproperty, mscs.resutilgetproperty, resapi/PRESUTIL_GET_PROPERTY, resapi/ResUtilGetProperty
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RESOURCE_EXIT_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilGetProperty
product: Windows
targetos: Windows
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
req.product: ADAM
---

# ResUtilGetProperty function


## -description


Returns a specified property from the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a>. The <b>PRESUTIL_GET_PROPERTY</b> type defines a pointer to this function.


## -parameters




### -param hkeyClusterKey [in]

Pointer to the cluster database key identifying the location of the property to retrieve.


### -param pPropertyTableItem [in]

Pointer to a  <a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a> structure that describes the property to retrieve.


### -param pOutPropertyItem [out]

Pointer to an output buffer in which to return the requested property. It is assumed that the buffer is part of a  <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a>.


### -param pcbOutPropertyItemSize [in, out]

Pointer to the size in bytes of the output buffer pointed to by <i>pOutPropertyItem</i>.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error code.




## -see-also




<a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a>
 

 


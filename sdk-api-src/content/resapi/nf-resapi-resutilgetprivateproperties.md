---
UID: NF:resapi.ResUtilGetPrivateProperties
title: ResUtilGetPrivateProperties function
author: windows-sdk-content
description: Returns private properties for a cluster object. The PRESUTIL_GET_PRIVATE_PROPERTIES type defines a pointer to this function.
old-location: mscs\resutilgetprivateproperties.htm
tech.root: MsCS
ms.assetid: 84019a77-4ecd-4618-ab7d-458c6c855dfd
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: PRESUTIL_GET_PRIVATE_PROPERTIES, PRESUTIL_GET_PRIVATE_PROPERTIES function [Failover Cluster], ResUtilGetPrivateProperties, ResUtilGetPrivateProperties function [Failover Cluster], _wolf_resutilgetprivateproperties, mscs.resutilgetprivateproperties, resapi/PRESUTIL_GET_PRIVATE_PROPERTIES, resapi/ResUtilGetPrivateProperties
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
 - ResUtilGetPrivateProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilGetPrivateProperties function


## -description


Returns  <a href="https://msdn.microsoft.com/a1dee11c-f1fe-4509-a40a-a58c4b8999ef">private properties</a> for a  <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster object</a>. The <b>PRESUTIL_GET_PRIVATE_PROPERTIES</b> type defines a pointer to this function.


## -parameters




### -param hkeyClusterKey [in]

Pointer to the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> key that identifies the location of the private properties to retrieve.


### -param pOutPropertyList [out]

Pointer to an output buffer in which a  <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a> with the names and values of the private properties is returned.


### -param cbOutPropertyListSize [in]

Size of the output buffer pointed to by <i>pOutPropertyList</i>.


### -param pcbBytesReturned [out]

Pointer to the total number of bytes in the property list pointed to by <i>pOutPropertyList</i>.


### -param pcbRequired [out]

Pointer to the number of bytes that is required if <i>pOutPropertyList</i> is too small to hold all of the private properties.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error codes.




## -see-also




<a href="https://msdn.microsoft.com/6ed03916-660f-4862-b638-900c9b8e4bef">ResUtilGetProperties</a>
 

 


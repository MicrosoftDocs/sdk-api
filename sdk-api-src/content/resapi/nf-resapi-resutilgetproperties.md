---
UID: NF:resapi.ResUtilGetProperties
title: ResUtilGetProperties function
author: windows-sdk-content
description: Retrieves properties specified by a property table from the cluster database and returns them in a property list. The PRESUTIL_GET_PROPERTIES type defines a pointer to this function.
old-location: mscs\resutilgetproperties.htm
tech.root: mscs
ms.assetid: 6ed03916-660f-4862-b638-900c9b8e4bef
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: PRESUTIL_GET_PROPERTIES, PRESUTIL_GET_PROPERTIES function [Failover Cluster], ResUtilGetProperties, ResUtilGetProperties function [Failover Cluster], _wolf_resutilgetproperties, mscs.resutilgetproperties, resapi/PRESUTIL_GET_PROPERTIES, resapi/ResUtilGetProperties
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
 - ResUtilGetProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilGetProperties function


## -description


Retrieves properties specified by a  <a href="https://msdn.microsoft.com/48591d73-606b-42b4-9711-4f7a84e9e971">property table</a> from 
    the <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> and returns them in a 
    <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a>. The 
    <b>PRESUTIL_GET_PROPERTIES</b> type defines a pointer to this function.


## -parameters




### -param hkeyClusterKey [in]

Pointer to the cluster database key that identifies the location of the properties to retrieve.


### -param pPropertyTable [in]

Pointer to an array of  <a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a> structures that describe the properties to retrieve.


### -param pOutPropertyList [out]

Pointer to an output buffer in which to return the property list.


### -param cbOutPropertyListSize [in]

Size in bytes of the output buffer pointed to by <i>pOutPropertyList</i>.


### -param pcbBytesReturned [out]

Pointer to the total number of bytes in the property list pointed to by <i>pOutPropertyList</i>.


### -param pcbRequired [out]

Pointer to the number of bytes that is required if <i>pOutPropertyList</i> is too small.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error codes.




## -see-also




<a href="https://msdn.microsoft.com/84019a77-4ecd-4618-ab7d-458c6c855dfd">ResUtilGetPrivateProperties</a>
 

 


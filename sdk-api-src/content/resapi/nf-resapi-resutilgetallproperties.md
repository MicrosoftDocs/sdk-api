---
UID: NF:resapi.ResUtilGetAllProperties
title: ResUtilGetAllProperties function
author: windows-sdk-content
description: Returns a property list that includes all of the default and unknown properties for a cluster object. The PRESUTIL_GET_ALL_PROPERTIES type defines a pointer to this function.
old-location: mscs\resutilgetallproperties.htm
tech.root: MsCS
ms.assetid: 18a27e1c-e709-4b0a-97c1-b0697deb8dc7
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: PRESUTIL_GET_ALL_PROPERTIES, PRESUTIL_GET_ALL_PROPERTIES function [Failover Cluster], ResUtilGetAllProperties, ResUtilGetAllProperties function [Failover Cluster], _wolf_resutilgetallproperties, mscs.resutilgetallproperties, resapi/PRESUTIL_GET_ALL_PROPERTIES, resapi/ResUtilGetAllProperties
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
 - ResUtilGetAllProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilGetAllProperties function


## -description


Returns a  <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a> that includes all of the default and  <a href="https://msdn.microsoft.com/1a4cc421-48b0-4dbe-8a1d-778f40cb77be">unknown</a> properties for a  <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster object</a>. The <b>PRESUTIL_GET_ALL_PROPERTIES</b> type defines a pointer to this function.


## -parameters




### -param hkeyClusterKey [in]

Pointer to the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> key that identifies the location of the properties to retrieve.


### -param pPropertyTable [in]

Pointer to an array of  <a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a> structures that describe the properties to retrieve.


### -param pOutPropertyList [out]

Pointer to an output buffer in which to return the property list.


### -param cbOutPropertyListSize [in]

Size in bytes of the output buffer pointed to by <i>OutBuffer</i>.


### -param pcbBytesReturned [out]

Pointer to the total number of bytes in the property list pointed to by <i>OutBuffer</i>.


### -param pcbRequired [out]

Pointer to the number of bytes that is required if <i>OutBuffer</i> is too small.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error codes.




## -remarks



The  <b>ResUtilGetAllProperties</b> utility function makes an entry in the property list for each property that is:

<ul>
<li>Included in the  <a href="https://msdn.microsoft.com/48591d73-606b-42b4-9711-4f7a84e9e971">property table</a>.</li>
<li>Included in the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> below the key identified by the <i>ClusterKey</i> parameter, regardless of whether the property is included in the property table.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a>
 

 


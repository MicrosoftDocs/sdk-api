---
UID: NF:resapi.ResUtilAddUnknownProperties
title: ResUtilAddUnknownProperties function
author: windows-sdk-content
description: Retrieves a set of unknown properties from the cluster database and appends them to the end of a property list.
old-location: mscs\resutiladdunknownproperties.htm
tech.root: mscs
ms.assetid: 17659c86-d7cc-4316-ba0e-ce71de727fa1
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: PRESUTIL_ADD_UNKNOWN_PROPERTIES, PRESUTIL_ADD_UNKNOWN_PROPERTIES function [Failover Cluster], ResUtilAddUnknownProperties, ResUtilAddUnknownProperties function [Failover Cluster], _wolf_resutiladdunknownproperties, mscs.resutiladdunknownproperties, resapi/PRESUTIL_ADD_UNKNOWN_PROPERTIES, resapi/ResUtilAddUnknownProperties
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
 - ResUtilAddUnknownProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilAddUnknownProperties function


## -description


Retrieves a set of  <a href="https://msdn.microsoft.com/1a4cc421-48b0-4dbe-8a1d-778f40cb77be">unknown properties</a> from the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> and appends them to the end of a  <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a>.


## -parameters




### -param hkeyClusterKey [in]

Pointer to the cluster database key that identifies the location for the properties to read.


### -param pPropertyTable [in]

Pointer to a  <a href="https://msdn.microsoft.com/48591d73-606b-42b4-9711-4f7a84e9e971">property table</a> describing the common and private properties of an object. Any properties found in the cluster database that are not in this property table are added to the property list.


### -param pOutPropertyList [in, out]

Pointer to a buffer in which to receive the returned properties. On input, the buffer can contain an existing property list, or it can be empty. On output, the retrieved properties will be appended to the end of the existing list, or, if the buffer is empty, will return as a new property list.


### -param pcbOutPropertyListSize [in]

Total byte size of the buffer pointed to by <i>pOutPropertyList</i>. The size of the buffer must be large enough to contain the existing property list and the property list to be returned.


### -param pcbBytesReturned [in, out]

On input, pointer to the byte size of the property list contained by the pOutPropertyList buffer. On output, pointer to the total number of bytes in the property list pointed to by <i>pOutPropertyList</i>.


### -param pcbRequired [in, out]

On output, points to the total number of bytes required to hold the returned property list. If the <i>pOutPropertyList</i> buffer was too small, it can be reallocated to the required size.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following is a possible error code.




## -remarks



The relationships between the input and output parameters of  <b>ResUtilAddUnknownProperties</b> are illustrated in the following diagram:

<img alt="" border="0" src="images/resutil.png"/>
The  <b>ResUtilAddUnknownProperties</b> utility function enumerates the properties stored in the cluster database (under <i>hkeyClusterKey</i>) and looks for corresponding properties in the property table (<i>pPropertyTable</i>). Each property that is listed in the cluster database but not listed in the property table is added to the property list (<i>pOutPropertyList</i>).




## -see-also




<a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a>



<a href="https://msdn.microsoft.com/ee729a3d-9d10-459c-b57d-de17f29d8ae8">ResUtilSetUnknownProperties</a>
 

 


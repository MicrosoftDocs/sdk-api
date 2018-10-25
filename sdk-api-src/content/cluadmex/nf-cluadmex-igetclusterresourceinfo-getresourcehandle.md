---
UID: NF:cluadmex.IGetClusterResourceInfo.GetResourceHandle
title: IGetClusterResourceInfo::GetResourceHandle
author: windows-sdk-content
description: Returns a handle to a resource.
old-location: mscs\igetclusterresourceinfo_getresourcehandle.htm
tech.root: mscs
ms.assetid: a03436da-e12a-45ac-9ac1-1d1896f87fd7
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: GetResourceHandle, GetResourceHandle method [Failover Cluster], GetResourceHandle method [Failover Cluster],IGetClusterResourceInfo interface, IGetClusterResourceInfo interface [Failover Cluster],GetResourceHandle method, IGetClusterResourceInfo.GetResourceHandle, IGetClusterResourceInfo::GetResourceHandle, _wolf_igetclusterresourceinfo_getresourcehandle, cluadmex/IGetClusterResourceInfo::GetResourceHandle, mscs.igetclusterresourceinfo_getresourcehandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: cluadmex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 Enterprise, Windows Server 2003 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CluAdmEx.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cluadmex.h
api_name:
 - IGetClusterResourceInfo.GetResourceHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGetClusterResourceInfo::GetResourceHandle


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns a handle to a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>.


## -parameters




### -param lObjIndex [in]

A number representing the zero-based index of the target resource. <i>lObjIndex</i> is 
       restricted to the number that can be retrieved by calling 
       <a href="https://msdn.microsoft.com/20ef63e2-bcec-48bc-86e8-ab746fb72cc5">IGetClusterDataInfo::GetObjectCount</a>.


## -returns



If <b>GetResourceHandle</b> is 
       successful, it returns a handle for the resource represented by <i>lObjIndex</i>.

If <b>GetResourceHandle</b> is 
       not successful, it returns <b>NULL</b>. For more information about the error, call the 
       function <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/20ef63e2-bcec-48bc-86e8-ab746fb72cc5">IGetClusterDataInfo::GetObjectCount</a>



<a href="https://msdn.microsoft.com/8a3a9e9d-4666-4d9a-83e3-10d667b42d66">IGetClusterResourceInfo</a>
 

 


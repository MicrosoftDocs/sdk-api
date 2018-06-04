---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IGetClusterResourceInfo::GetResourceNetworkName


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns the name of the <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a> managed by the 
    <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">Network Name</a> resource on which a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> depends.


## -parameters




### -param lObjIndex [in]

A number representing the zero-based index of the target resource. The target resource may or may not depend 
       on a Network Name resource. <i>lObjIndex</i> is restricted to the number that can be 
       retrieved by calling 
       <a href="https://msdn.microsoft.com/20ef63e2-bcec-48bc-86e8-ab746fb72cc5">IGetClusterDataInfo::GetObjectCount</a>.


### -param lpszNetName [out]

Pointer to a null-terminated Unicode string containing the name of the network upon which the resource 
       indexed by <i>lObjIndex</i> depends. Although declared as a 
       <b>BSTR</b>, this parameter is implemented as an <b>LPWSTR</b>.


### -param pcchNetName [in, out]

Pointer to the maximum count in characters of the buffer pointed to by <i>lpszNetName</i>. 
       On input, this value should be large enough to contain <b>MAX_COMPUTERNAME_LENGTH</b> + 1 
       characters. On output, <i>pcchNetName</i> points to the actual number of characters copied 
       to the content of <i>lpszNetName</i>.


## -returns



This method returns BOOL.




## -remarks



The 
     <b>GetResourceNetworkName</b> 
     method is necessary to allow 
     <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> extension property 
     pages to determine whether a resource has an existing or a pending dependency on a Network Name resource.

The name of the network is stored in the Network Name resource's Name private property. The Network Name 
     resource's Name common property is the name of the resource, not the network.

<b>MAX_COMPUTERNAME_LENGTH</b> is a constant defined as 15 in the Windows header file 
     WinBase.h.




## -see-also




<a href="https://msdn.microsoft.com/20ef63e2-bcec-48bc-86e8-ab746fb72cc5">IGetClusterDataInfo::GetObjectCount</a>



<a href="https://msdn.microsoft.com/8a3a9e9d-4666-4d9a-83e3-10d667b42d66">IGetClusterResourceInfo</a>
 

 


---
UID: NF:cluadmex.IGetClusterNetInterfaceInfo.GetNetInterfaceHandle
title: IGetClusterNetInterfaceInfo::GetNetInterfaceHandle
author: windows-sdk-content
description: Retrieves a handle to a node.
old-location: mscs\igetclusternetinterfaceinfo_getnetinterfacehandle.htm
tech.root: mscs
ms.assetid: a11ebbed-72e3-4f57-af8d-8a14c4b0fad2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetNetInterfaceHandle, GetNetInterfaceHandle method [Failover Cluster], GetNetInterfaceHandle method [Failover Cluster],IGetClusterNetInterfaceInfo interface, IGetClusterNetInterfaceInfo interface [Failover Cluster],GetNetInterfaceHandle method, IGetClusterNetInterfaceInfo.GetNetInterfaceHandle, IGetClusterNetInterfaceInfo::GetNetInterfaceHandle, _wolf_igetclusternetinterfaceinfo_getnetinterfacehandle, cluadmex/IGetClusterNetInterfaceInfo::GetNetInterfaceHandle, mscs.igetclusternetinterfaceinfo_getnetinterfacehandle
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
 - IGetClusterNetInterfaceInfo.GetNetInterfaceHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGetClusterNetInterfaceInfo::GetNetInterfaceHandle


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Retrieves a handle to a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>.


## -parameters




### -param lObjIndex [in]

A number representing the zero-based index of the target network interface. 
       <i>lObjIndex</i> is restricted to the number that can be retrieved by calling 
       <a href="https://msdn.microsoft.com/20ef63e2-bcec-48bc-86e8-ab746fb72cc5">IGetClusterDataInfo::GetObjectCount</a>.


## -returns



If 
       <b>GetNetInterfaceHandle</b> 
       is successful, it returns a handle for the network interface represented by 
       <i>lObjIndex</i>.

If 
       <b>GetNetInterfaceHandle</b> 
       is not successful, it returns <b>NULL</b>. For more information about the error, call the 
       function <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Do not close the handle obtained through this method.




## -see-also




<a href="https://msdn.microsoft.com/20ef63e2-bcec-48bc-86e8-ab746fb72cc5">IGetClusterDataInfo::GetObjectCount</a>



<a href="https://msdn.microsoft.com/c7a0ee81-e263-4a2d-a0e5-18d3a4ad0d79">IGetClusterNetInterfaceInfo</a>
 

 


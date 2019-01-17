---
UID: NF:cluadmex.IGetClusterNodeInfo.GetNodeHandle
title: IGetClusterNodeInfo::GetNodeHandle
author: windows-sdk-content
description: Returns a handle to a node.
old-location: mscs\igetclusternodeinfo_getnodehandle.htm
tech.root: MsCS
ms.assetid: d1932844-9900-4a16-8c9a-39f89bddfdb0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetNodeHandle, GetNodeHandle method [Failover Cluster], GetNodeHandle method [Failover Cluster],IGetClusterNodeInfo interface, IGetClusterNodeInfo interface [Failover Cluster],GetNodeHandle method, IGetClusterNodeInfo.GetNodeHandle, IGetClusterNodeInfo::GetNodeHandle, _wolf_igetclusternodeinfo_getnodehandle, cluadmex/IGetClusterNodeInfo::GetNodeHandle, mscs.igetclusternodeinfo_getnodehandle
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
 - IGetClusterNodeInfo.GetNodeHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGetClusterNodeInfo::GetNodeHandle


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns a handle to a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>.


## -parameters




### -param lObjIndex [in]

A number representing the zero-based index of the target node. <i>lObjIndex</i> is 
       restricted to the number that can be retrieved by calling 
       <a href="https://msdn.microsoft.com/20ef63e2-bcec-48bc-86e8-ab746fb72cc5">IGetClusterDataInfo::GetObjectCount</a>.


## -returns



If <b>GetNodeHandle</b> is successful, 
       it returns a handle for the node represented by <i>lObjIndex</i>.

If <b>GetNodeHandle</b> is not 
       successful, it returns <b>NULL</b>. For more information about the error, call the function 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Do not close the handle obtained through this method.




## -see-also




<a href="https://msdn.microsoft.com/20ef63e2-bcec-48bc-86e8-ab746fb72cc5">IGetClusterDataInfo::GetObjectCount</a>



<a href="https://msdn.microsoft.com/97c90830-1f6d-4f8f-ba0a-fee39aef5c1d">IGetClusterNodeInfo</a>
 

 


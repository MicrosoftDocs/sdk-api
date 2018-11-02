---
UID: NF:clusapi.SetClusterServiceAccountPassword
title: SetClusterServiceAccountPassword function
author: windows-sdk-content
description: Changes the password for the Cluster service user account on all available cluster nodes.
old-location: mscs\setclusterserviceaccountpassword.htm
tech.root: mscs
ms.assetid: 4afadb62-2bea-46ef-b0d6-e327ac96d16f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CLUSTER_SET_PASSWORD_IGNORE_DOWN_NODES, PCLUSAPI_SET_CLUSTER_SERVICE_ACCOUNT_PASSWORD, PCLUSAPI_SET_CLUSTER_SERVICE_ACCOUNT_PASSWORD function [Failover Cluster], SetClusterServiceAccountPassword, SetClusterServiceAccountPassword function [Failover Cluster], _wolf_setclusterserviceaccountpassword, clusapi/PCLUSAPI_SET_CLUSTER_SERVICE_ACCOUNT_PASSWORD, clusapi/SetClusterServiceAccountPassword, mscs.setclusterserviceaccountpassword
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 Datacenter, Windows Server 2003 Enterprise
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - SetClusterServiceAccountPassword
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetClusterServiceAccountPassword function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems specified in the 
    Requirements section. Support for this function was removed in Windows Server 2008 and this function does 
    nothing and returns <b>ERROR_CALL_NOT_IMPLEMENTED</b>.]

Changes the password for the Cluster service user account on all available cluster 
    nodes. The <b>PCLUSAPI_SET_CLUSTER_SERVICE_ACCOUNT_PASSWORD</b> type defines a pointer to this function.


## -parameters




### -param lpszClusterName [in]

<b>NULL</b>-terminated Unicode string specifying the name of the cluster.


### -param lpszNewPassword [in]

<b>NULL</b>-terminated Unicode string specifying the new password for the Cluster service 
       user account.


### -param dwFlags [in, optional]

Optional bitfield of values enumerated from the 
       <a href="https://msdn.microsoft.com/8d202e08-c8ff-4bc6-a1ea-6bdb7ba4937e">CLUSTER_SET_PASSWORD_FLAGS</a> enumeration 
       containing flags that describe how the password update is to be applied to the cluster.

By default (<i>dwFlags</i> = 0), the function will not proceed unless all cluster nodes 
       are available.



#### CLUSTER_SET_PASSWORD_IGNORE_DOWN_NODES (1 (0x1))

Causes the 
         <b>SetClusterServiceAccountPassword</b> 
         function to proceed even if all nodes are not available. The function will attempt to change the password on 
         as many nodes as it can, but any nodes not in the <b>ClusterNodeUp</b> or 
         <b>ClusterNodePaused</b> states (see 
         <a href="https://msdn.microsoft.com/94c83582-3d99-4a20-ad58-1af4e8190781">GetClusterNodeState</a>) will not be updated.


### -param lpReturnStatusBuffer [out]

Pointer to an output buffer that receives an array of 
       <a href="https://msdn.microsoft.com/en-us/library/Aa369164(v=VS.85).aspx">CLUSTER_SET_PASSWORD_STATUS</a> structures 
       describing the result of the password update for each cluster node. If this parameter is not 
       <b>NULL</b> and the buffer is not large enough to hold the resulting data, the function 
       returns <b>ERROR_MORE_DATA</b> and sets <i>lpcbReturnStatusBufferSize</i> 
       to the required size for the output buffer. If this parameter is <b>NULL</b>, no password 
       update will be performed; the function will set <i>lpcbReturnStatusBufferSize</i> to the 
       required buffer size and return <b>ERROR_SUCCESS</b>.


### -param lpcbReturnStatusBufferSize [in, out]

On input, pointer to a value specifying the size (in bytes) of the output buffer. On output, pointer to a 
       value specifying the actual size (in bytes) of the resulting data. The output size is always specified, even if 
       <i>lpReturnStatusBuffer</i> is <b>NULL</b>. This parameter cannot be 
       <b>NULL</b>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
      <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error 
      codes.




## -remarks



By default, the 
     <b>SetClusterServiceAccountPassword</b> 
     function does nothing unless all nodes in the cluster are available (that is, in the 
     <b>ClusterNodeStateUp</b> or <b>ClusterNodeStatePaused</b> states). You 
     can use the <b>CLUSTER_SET_PASSWORD_IGNORE_DOWN_NODES</b> flag to override this behavior, 
     but note that any node that fails to update the password will be unable to join the cluster until the password is 
     manually updated on that node.

If the new password is the same as the old password on a node, the password update is not applied to that node 
     and <b>ERROR_SUCCESS</b> is returned.

This function does not update the password stored by the domain controllers for the Cluster service user 
     account.

Do not call 
     <b>SetClusterServiceAccountPassword</b> 
     from a resource DLL.




## -see-also




<a href="https://msdn.microsoft.com/8d202e08-c8ff-4bc6-a1ea-6bdb7ba4937e">CLUSTER_SET_PASSWORD_FLAGS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369164(v=VS.85).aspx">CLUSTER_SET_PASSWORD_STATUS</a>



<a href="https://msdn.microsoft.com/1b3a3b23-39db-47b7-b4a8-17fc1ee45df6">Cluster Management Functions</a>
 

 


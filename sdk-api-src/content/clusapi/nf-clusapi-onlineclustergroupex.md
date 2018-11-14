---
UID: NF:clusapi.OnlineClusterGroupEx
title: OnlineClusterGroupEx function
author: windows-sdk-content
description: Brings a group online.
old-location: mscs\onlineclustergroupex.htm
tech.root: mscs
ms.assetid: F79E75E9-EB54-4C66-AB7C-98AF075718B1
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: CLUSAPI_GROUP_ONLINE_BEST_POSSIBLE_NODE, CLUSAPI_GROUP_ONLINE_IGNORE_RESOURCE_STATUS, CLUSAPI_GROUP_ONLINE_SYNCHRONOUS, OnlineClusterGroupEx, OnlineClusterGroupEx function [Failover Cluster], clusapi/OnlineClusterGroupEx, mscs.onlineclustergroupex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - OnlineClusterGroupEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- OnlineClusterGroupEx
: 
---

# OnlineClusterGroupEx function


## -description


Brings a  <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group</a> online.


## -parameters




### -param hGroup [in]

A handle to the group to be brought online.


### -param hDestinationNode [in, optional]

A handle to the  <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> that is to host the group.


### -param dwOnlineFlags [in]

A flag that specifies settings for the resource that is to be brought online.



#### CLUSAPI_GROUP_ONLINE_IGNORE_RESOURCE_STATUS (0x00000001)

The server is to ignore locked mode for the resource.



#### CLUSAPI_GROUP_ONLINE_SYNCHRONOUS (0x00000002)

Use a synchronous operation to bring the group online.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This value was added in Windows Server 2016.



#### CLUSAPI_GROUP_ONLINE_BEST_POSSIBLE_NODE (0x00000004)

Let the cluster service is to determine the node that will host the group when it is brought online.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This value was added in Windows Server 2016.



#### 0

The server is  not to  ignore locked mode for the resource.


### -param lpInBuffer [in, optional]

A pointer to the input buffer that receives instructions for the operation.  The <i>lpInBuffer</i>  parameter is formatted as a property list.


### -param cbInBufferSize [in]

The size of the <i>lpInBuffer</i> parameter, in bytes.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>. The following are possible error codes.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369686(v=VS.85).aspx">Group Management Functions</a>
 

 


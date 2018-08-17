---
UID: NC:clusapi.PCLUSAPI_OPEN_CLUSTER_GROUP_EX
title: PCLUSAPI_OPEN_CLUSTER_GROUP_EX
author: windows-sdk-content
description: Opens a failover cluster group and returns a handle to it.
old-location: mscs\openclustergroupex.htm
old-project: mscs
ms.assetid: 240defbb-b9e9-4455-b863-c9b2192f12b7
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_OPEN_CLUSTER_GROUP_EX, PCLUSAPI_OPEN_CLUSTER_GROUP_EX callback, PCLUSAPI_OPEN_CLUSTER_GROUP_EX callback function [Failover Cluster], clusapi/PCLUSAPI_OPEN_CLUSTER_GROUP_EX, mscs.openclustergroupex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSAPI_OPEN_CLUSTER_GROUP_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_OPEN_CLUSTER_GROUP_EX callback function


## -description


Opens a failover cluster <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> and returns a handle to 
    it.


## -parameters




### -param hCluster [in]

Handle to a cluster that includes the group to open.


### -param lpszGroupName [in, optional]

Name of the group to open.


### -param dwDesiredAccess [in]

The requested access privileges. This may be any combination of <b>GENERIC_READ</b> 
      (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> 
      (0x02000000). If this value is zero (0) and undefined error may be returned. Using 
      <b>GENERIC_ALL</b> is the same as calling 
      <a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>.


### -param lpdwGrantedAccess [out, optional]

Optional parameter that contains the address of a <b>DWORD</b> that will receive the 
      access rights granted. If the <i>DesiredAccess</i> parameter is 
      <b>MAXIMUM_ALLOWED</b> (0x02000000) then the <b>DWORD</b> pointed to by 
      this parameter will contain the maximum privileges granted to this user.


## -returns



If the operation was successful, 
      <i>OpenClusterGroupEx</i> returns a group handle.




## -see-also




<a href="https://msdn.microsoft.com/5bbacf45-2e1a-402a-8592-c8f60034c4ad">CloseClusterGroup</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369686(v=VS.85).aspx">Group Management Functions</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 


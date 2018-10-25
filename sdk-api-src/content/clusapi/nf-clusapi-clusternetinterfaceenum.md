---
UID: NF:clusapi.ClusterNetInterfaceEnum
title: ClusterNetInterfaceEnum function
author: windows-sdk-content
description: Enumerates the network interfaces installed on a cluster, returning one name with each call.
old-location: mscs\clusternetinterfaceenum.htm
tech.root: mscs
ms.assetid: 691362e9-88ba-4f10-8fde-eebcc72157b4
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: ClusterNetInterfaceEnum, ClusterNetInterfaceEnum function [Failover Cluster], clusapi/ClusterNetInterfaceEnum, mscs.clusternetinterfaceenum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
 - ClusterNetInterfaceEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterNetInterfaceEnum function


## -description


Enumerates the <a href="https://msdn.microsoft.com/en-us/library/Aa371519(v=VS.85).aspx">network interfaces</a> installed on a 
    cluster, returning one name with each call.


## -parameters




### -param hNetInterfaceEnum [in]

Handle to an existing enumeration object originally returned by the 
       <a href="https://msdn.microsoft.com/en-us/library/Mt705443(v=VS.85).aspx">ClusterNetInterfaceOpenEnum</a> function.


### -param dwIndex [in]

Index used to identify the entry to be enumerated. This parameter should be zero for the first call and then incremented for each subsequent 
       call.


### -param lpszName [out]

Pointer to a null-terminated Unicode string containing the name of the returned object.


### -param lpcchName [in, out]

Pointer to the size, in characters, of the <i>lpszName</i> buffer. On input, 
       specify the maximum number of characters the buffer can hold, including the terminating 
       <b>NULL</b>. On output, indicates the number of characters in the resulting name, excluding 
       the terminating <b>NULL</b>.


## -returns



The function returns one of the following values.




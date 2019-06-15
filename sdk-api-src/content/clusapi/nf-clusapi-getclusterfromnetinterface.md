---
UID: NF:clusapi.GetClusterFromNetInterface
title: GetClusterFromNetInterface function (clusapi.h)
author: windows-sdk-content
description: Returns a handle to the cluster associated with a network interface.
old-location: mscs\getclusterfromnetinterface.htm
tech.root: MsCS
ms.assetid: 7c6c6883-0d88-4162-a70d-cb6f1153226e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetClusterFromNetInterface, GetClusterFromNetInterface function [Failover Cluster], PCLUSAPI_GET_CLUSTER_FROM_NET_INTERFACE, PCLUSAPI_GET_CLUSTER_FROM_NET_INTERFACE function [Failover Cluster], _wolf_getclusterfromnetinterface, clusapi/GetClusterFromNetInterface, clusapi/PCLUSAPI_GET_CLUSTER_FROM_NET_INTERFACE, mscs.getclusterfromnetinterface
ms.topic: function
f1_keywords: ["clusapi/GetClusterFromNetInterface"]
req.header: clusapi.h
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
 - GetClusterFromNetInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetClusterFromNetInterface function


## -description


Returns a handle to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/c-gly">cluster</a> associated with a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/network-interfaces">network interface</a>. The <b>PCLUSAPI_GET_CLUSTER_FROM_NET_INTERFACE</b> type defines a pointer to this function.


## -parameters




### -param hNetInterface [in]

Handle to the network interface.


## -returns



If the operation succeeds, the function returns a handle to the cluster that owns the network interface.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



For <i>hNetInterface</i> to be a valid handle, there must necessarily be an open cluster handle (see  <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-openclusternetinterface">OpenClusterNetInterface</a>).  <b>GetClusterFromNetInterface</b> returns another instance of the handle from which <i>hNetInterface</i> was obtained.

Be sure to call  <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-closecluster">CloseCluster</a> on the handle returned from  <b>GetClusterFromNetInterface</b> before the handle goes out of scope. Closing this handle does not invalidate <i>hNetInterface</i> or the cluster handle from which <i>hNetInterface</i> was obtained.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-closecluster">CloseCluster</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-closeclusternetinterface">CloseClusterNetInterface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-getclusterfromgroup">GetClusterFromGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-getclusterfromnetwork">GetClusterFromNetwork</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-getclusterfromnode">GetClusterFromNode</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-getclusterfromresource">GetClusterFromResource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-openclusternetinterface">OpenClusterNetInterface</a>
 

 


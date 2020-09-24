---
UID: NF:cluadmex.IGetClusterNodeInfo.GetNodeHandle
title: IGetClusterNodeInfo::GetNodeHandle (cluadmex.h)
description: Returns a handle to a node.
helpviewer_keywords: ["GetNodeHandle","GetNodeHandle method [Failover Cluster]","GetNodeHandle method [Failover Cluster]","IGetClusterNodeInfo interface","IGetClusterNodeInfo interface [Failover Cluster]","GetNodeHandle method","IGetClusterNodeInfo.GetNodeHandle","IGetClusterNodeInfo::GetNodeHandle","_wolf_igetclusternodeinfo_getnodehandle","cluadmex/IGetClusterNodeInfo::GetNodeHandle","mscs.igetclusternodeinfo_getnodehandle"]
old-location: mscs\igetclusternodeinfo_getnodehandle.htm
tech.root: MsCS
ms.assetid: d1932844-9900-4a16-8c9a-39f89bddfdb0
ms.date: 12/05/2018
ms.keywords: GetNodeHandle, GetNodeHandle method [Failover Cluster], GetNodeHandle method [Failover Cluster],IGetClusterNodeInfo interface, IGetClusterNodeInfo interface [Failover Cluster],GetNodeHandle method, IGetClusterNodeInfo.GetNodeHandle, IGetClusterNodeInfo::GetNodeHandle, _wolf_igetclusternodeinfo_getnodehandle, cluadmex/IGetClusterNodeInfo::GetNodeHandle, mscs.igetclusternodeinfo_getnodehandle
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGetClusterNodeInfo::GetNodeHandle
 - cluadmex/IGetClusterNodeInfo::GetNodeHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cluadmex.h
api_name:
 - IGetClusterNodeInfo.GetNodeHandle
---

# IGetClusterNodeInfo::GetNodeHandle


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns a handle to a <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>.

## -parameters

### -param lObjIndex [in]

A number representing the zero-based index of the target node. <i>lObjIndex</i> is 
       restricted to the number that can be retrieved by calling 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getobjectcount">IGetClusterDataInfo::GetObjectCount</a>.

## -returns

If <b>GetNodeHandle</b> is successful, 
       it returns a handle for the node represented by <i>lObjIndex</i>.

If <b>GetNodeHandle</b> is not 
       successful, it returns <b>NULL</b>. For more information about the error, call the function 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Do not close the handle obtained through this method.

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getobjectcount">IGetClusterDataInfo::GetObjectCount</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternodeinfo">IGetClusterNodeInfo</a>
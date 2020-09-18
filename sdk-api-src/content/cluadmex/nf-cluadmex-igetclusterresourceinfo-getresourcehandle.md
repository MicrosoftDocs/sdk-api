---
UID: NF:cluadmex.IGetClusterResourceInfo.GetResourceHandle
title: IGetClusterResourceInfo::GetResourceHandle (cluadmex.h)
description: Returns a handle to a resource.
helpviewer_keywords: ["GetResourceHandle","GetResourceHandle method [Failover Cluster]","GetResourceHandle method [Failover Cluster]","IGetClusterResourceInfo interface","IGetClusterResourceInfo interface [Failover Cluster]","GetResourceHandle method","IGetClusterResourceInfo.GetResourceHandle","IGetClusterResourceInfo::GetResourceHandle","_wolf_igetclusterresourceinfo_getresourcehandle","cluadmex/IGetClusterResourceInfo::GetResourceHandle","mscs.igetclusterresourceinfo_getresourcehandle"]
old-location: mscs\igetclusterresourceinfo_getresourcehandle.htm
tech.root: MsCS
ms.assetid: a03436da-e12a-45ac-9ac1-1d1896f87fd7
ms.date: 12/05/2018
ms.keywords: GetResourceHandle, GetResourceHandle method [Failover Cluster], GetResourceHandle method [Failover Cluster],IGetClusterResourceInfo interface, IGetClusterResourceInfo interface [Failover Cluster],GetResourceHandle method, IGetClusterResourceInfo.GetResourceHandle, IGetClusterResourceInfo::GetResourceHandle, _wolf_igetclusterresourceinfo_getresourcehandle, cluadmex/IGetClusterResourceInfo::GetResourceHandle, mscs.igetclusterresourceinfo_getresourcehandle
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
 - IGetClusterResourceInfo::GetResourceHandle
 - cluadmex/IGetClusterResourceInfo::GetResourceHandle
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
 - IGetClusterResourceInfo.GetResourceHandle
---

# IGetClusterResourceInfo::GetResourceHandle


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns a handle to a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>.

## -parameters

### -param lObjIndex [in]

A number representing the zero-based index of the target resource. <i>lObjIndex</i> is 
       restricted to the number that can be retrieved by calling 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getobjectcount">IGetClusterDataInfo::GetObjectCount</a>.

## -returns

If <b>GetResourceHandle</b> is 
       successful, it returns a handle for the resource represented by <i>lObjIndex</i>.

If <b>GetResourceHandle</b> is 
       not successful, it returns <b>NULL</b>. For more information about the error, call the 
       function <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getobjectcount">IGetClusterDataInfo::GetObjectCount</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterresourceinfo">IGetClusterResourceInfo</a>
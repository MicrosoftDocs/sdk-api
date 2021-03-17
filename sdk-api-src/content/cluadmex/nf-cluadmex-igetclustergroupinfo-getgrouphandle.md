---
UID: NF:cluadmex.IGetClusterGroupInfo.GetGroupHandle
title: IGetClusterGroupInfo::GetGroupHandle (cluadmex.h)
description: Returns a handle to a group.
helpviewer_keywords: ["GetGroupHandle","GetGroupHandle method [Failover Cluster]","GetGroupHandle method [Failover Cluster]","IGetClusterGroupInfo interface","IGetClusterGroupInfo interface [Failover Cluster]","GetGroupHandle method","IGetClusterGroupInfo.GetGroupHandle","IGetClusterGroupInfo::GetGroupHandle","_wolf_igetclustergroupinfo_getgrouphandle","cluadmex/IGetClusterGroupInfo::GetGroupHandle","mscs.igetclustergroupinfo_getgrouphandle"]
old-location: mscs\igetclustergroupinfo_getgrouphandle.htm
tech.root: MsCS
ms.assetid: b578b3fa-9c3d-4f94-b35f-ba0fbe1fdd40
ms.date: 12/05/2018
ms.keywords: GetGroupHandle, GetGroupHandle method [Failover Cluster], GetGroupHandle method [Failover Cluster],IGetClusterGroupInfo interface, IGetClusterGroupInfo interface [Failover Cluster],GetGroupHandle method, IGetClusterGroupInfo.GetGroupHandle, IGetClusterGroupInfo::GetGroupHandle, _wolf_igetclustergroupinfo_getgrouphandle, cluadmex/IGetClusterGroupInfo::GetGroupHandle, mscs.igetclustergroupinfo_getgrouphandle
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
 - IGetClusterGroupInfo::GetGroupHandle
 - cluadmex/IGetClusterGroupInfo::GetGroupHandle
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
 - IGetClusterGroupInfo.GetGroupHandle
---

# IGetClusterGroupInfo::GetGroupHandle


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns a handle to a <a href="/previous-versions/windows/desktop/mscs/groups">group</a>.

## -parameters

### -param lObjIndex [in]

A number representing the zero-based index of the target group. <i>lObjIndex</i> is 
       restricted to the number that can be retrieved by calling 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getobjectcount">IGetClusterDataInfo::GetObjectCount</a>.

## -returns

If <b>GetGroupHandle</b> is 
       successful, it returns a handle for the group represented by <i>lObjIndex</i>.

If <b>GetGroupHandle</b> is not 
       successful, it returns <b>NULL</b>. For more information about the error, call the function 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Do not close the handle obtained through this method.

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getobjectcount">IGetClusterDataInfo::GetObjectCount</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclustergroupinfo">IGetClusterGroupInfo</a>
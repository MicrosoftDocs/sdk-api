---
UID: NF:cluadmex.IGetClusterNetworkInfo.GetNetworkHandle
title: IGetClusterNetworkInfo::GetNetworkHandle (cluadmex.h)
description: Retrieves a handle to a network.
helpviewer_keywords: ["GetNetworkHandle","GetNetworkHandle method [Failover Cluster]","GetNetworkHandle method [Failover Cluster]","IGetClusterNetworkInfo interface","IGetClusterNetworkInfo interface [Failover Cluster]","GetNetworkHandle method","IGetClusterNetworkInfo.GetNetworkHandle","IGetClusterNetworkInfo::GetNetworkHandle","_wolf_igetclusternetworkinfo_getnetworkhandle","cluadmex/IGetClusterNetworkInfo::GetNetworkHandle","mscs.igetclusternetworkinfo_getnetworkhandle"]
old-location: mscs\igetclusternetworkinfo_getnetworkhandle.htm
tech.root: MsCS
ms.assetid: 596ebdb3-c4c1-4186-ac6b-e6a7d4a61688
ms.date: 12/05/2018
ms.keywords: GetNetworkHandle, GetNetworkHandle method [Failover Cluster], GetNetworkHandle method [Failover Cluster],IGetClusterNetworkInfo interface, IGetClusterNetworkInfo interface [Failover Cluster],GetNetworkHandle method, IGetClusterNetworkInfo.GetNetworkHandle, IGetClusterNetworkInfo::GetNetworkHandle, _wolf_igetclusternetworkinfo_getnetworkhandle, cluadmex/IGetClusterNetworkInfo::GetNetworkHandle, mscs.igetclusternetworkinfo_getnetworkhandle
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
 - IGetClusterNetworkInfo::GetNetworkHandle
 - cluadmex/IGetClusterNetworkInfo::GetNetworkHandle
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
 - IGetClusterNetworkInfo.GetNetworkHandle
---

# IGetClusterNetworkInfo::GetNetworkHandle


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Retrieves a handle to a <a href="/previous-versions/windows/desktop/mscs/networks">network</a>.

## -parameters

### -param lObjIndex [in]

A number representing the zero-based index of the target network. <i>lObjIndex</i> is 
       restricted to the number that can be retrieved by calling 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getobjectcount">IGetClusterDataInfo::GetObjectCount</a>.

## -returns

If <b>GetNetworkHandle</b> is 
       successful, it returns a handle for the network represented by <i>lObjIndex</i>.

If <b>GetNetworkHandle</b> is not 
       successful, it returns <b>NULL</b>. For more information about the error, call the function 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Do not close the handle obtained through this method.

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getobjectcount">IGetClusterDataInfo::GetObjectCount</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternetworkinfo">IGetClusterNetworkInfo</a>
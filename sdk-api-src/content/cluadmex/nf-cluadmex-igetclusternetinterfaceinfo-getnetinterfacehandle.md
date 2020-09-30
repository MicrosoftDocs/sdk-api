---
UID: NF:cluadmex.IGetClusterNetInterfaceInfo.GetNetInterfaceHandle
title: IGetClusterNetInterfaceInfo::GetNetInterfaceHandle (cluadmex.h)
description: Retrieves a handle to a node.
helpviewer_keywords: ["GetNetInterfaceHandle","GetNetInterfaceHandle method [Failover Cluster]","GetNetInterfaceHandle method [Failover Cluster]","IGetClusterNetInterfaceInfo interface","IGetClusterNetInterfaceInfo interface [Failover Cluster]","GetNetInterfaceHandle method","IGetClusterNetInterfaceInfo.GetNetInterfaceHandle","IGetClusterNetInterfaceInfo::GetNetInterfaceHandle","_wolf_igetclusternetinterfaceinfo_getnetinterfacehandle","cluadmex/IGetClusterNetInterfaceInfo::GetNetInterfaceHandle","mscs.igetclusternetinterfaceinfo_getnetinterfacehandle"]
old-location: mscs\igetclusternetinterfaceinfo_getnetinterfacehandle.htm
tech.root: MsCS
ms.assetid: a11ebbed-72e3-4f57-af8d-8a14c4b0fad2
ms.date: 12/05/2018
ms.keywords: GetNetInterfaceHandle, GetNetInterfaceHandle method [Failover Cluster], GetNetInterfaceHandle method [Failover Cluster],IGetClusterNetInterfaceInfo interface, IGetClusterNetInterfaceInfo interface [Failover Cluster],GetNetInterfaceHandle method, IGetClusterNetInterfaceInfo.GetNetInterfaceHandle, IGetClusterNetInterfaceInfo::GetNetInterfaceHandle, _wolf_igetclusternetinterfaceinfo_getnetinterfacehandle, cluadmex/IGetClusterNetInterfaceInfo::GetNetInterfaceHandle, mscs.igetclusternetinterfaceinfo_getnetinterfacehandle
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
 - IGetClusterNetInterfaceInfo::GetNetInterfaceHandle
 - cluadmex/IGetClusterNetInterfaceInfo::GetNetInterfaceHandle
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
 - IGetClusterNetInterfaceInfo.GetNetInterfaceHandle
---

# IGetClusterNetInterfaceInfo::GetNetInterfaceHandle


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Retrieves a handle to a <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>.

## -parameters

### -param lObjIndex [in]

A number representing the zero-based index of the target network interface. 
       <i>lObjIndex</i> is restricted to the number that can be retrieved by calling 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getobjectcount">IGetClusterDataInfo::GetObjectCount</a>.

## -returns

If 
       <b>GetNetInterfaceHandle</b> 
       is successful, it returns a handle for the network interface represented by 
       <i>lObjIndex</i>.

If 
       <b>GetNetInterfaceHandle</b> 
       is not successful, it returns <b>NULL</b>. For more information about the error, call the 
       function <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Do not close the handle obtained through this method.

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getobjectcount">IGetClusterDataInfo::GetObjectCount</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternetinterfaceinfo">IGetClusterNetInterfaceInfo</a>
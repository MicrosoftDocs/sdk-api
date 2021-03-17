---
UID: NF:cluadmex.IGetClusterResourceInfo.GetResourceNetworkName
title: IGetClusterResourceInfo::GetResourceNetworkName (cluadmex.h)
description: Returns the name of the network managed by the Network Name resource on which a resource depends.
helpviewer_keywords: ["GetResourceNetworkName","GetResourceNetworkName method [Failover Cluster]","GetResourceNetworkName method [Failover Cluster]","IGetClusterResourceInfo interface","IGetClusterResourceInfo interface [Failover Cluster]","GetResourceNetworkName method","IGetClusterResourceInfo.GetResourceNetworkName","IGetClusterResourceInfo::GetResourceNetworkName","_wolf_igetclusterresourceinfo_getresourcenetworkname","cluadmex/IGetClusterResourceInfo::GetResourceNetworkName","mscs.igetclusterresourceinfo_getresourcenetworkname"]
old-location: mscs\igetclusterresourceinfo_getresourcenetworkname.htm
tech.root: MsCS
ms.assetid: 5c4a16ab-b71c-49f6-95cb-8627eaffb8d6
ms.date: 12/05/2018
ms.keywords: GetResourceNetworkName, GetResourceNetworkName method [Failover Cluster], GetResourceNetworkName method [Failover Cluster],IGetClusterResourceInfo interface, IGetClusterResourceInfo interface [Failover Cluster],GetResourceNetworkName method, IGetClusterResourceInfo.GetResourceNetworkName, IGetClusterResourceInfo::GetResourceNetworkName, _wolf_igetclusterresourceinfo_getresourcenetworkname, cluadmex/IGetClusterResourceInfo::GetResourceNetworkName, mscs.igetclusterresourceinfo_getresourcenetworkname
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
 - IGetClusterResourceInfo::GetResourceNetworkName
 - cluadmex/IGetClusterResourceInfo::GetResourceNetworkName
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
 - IGetClusterResourceInfo.GetResourceNetworkName
---

# IGetClusterResourceInfo::GetResourceNetworkName


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns the name of the <a href="/previous-versions/windows/desktop/mscs/networks">network</a> managed by the 
    <a href="/previous-versions/windows/desktop/mscs/network-name">Network Name</a> resource on which a 
    <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> depends.

## -parameters

### -param lObjIndex [in]

A number representing the zero-based index of the target resource. The target resource may or may not depend 
       on a Network Name resource. <i>lObjIndex</i> is restricted to the number that can be 
       retrieved by calling 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getobjectcount">IGetClusterDataInfo::GetObjectCount</a>.

### -param lpszNetName [out]

Pointer to a null-terminated Unicode string containing the name of the network upon which the resource 
       indexed by <i>lObjIndex</i> depends. Although declared as a 
       <b>BSTR</b>, this parameter is implemented as an <b>LPWSTR</b>.

### -param pcchNetName [in, out]

Pointer to the maximum count in characters of the buffer pointed to by <i>lpszNetName</i>. 
       On input, this value should be large enough to contain <b>MAX_COMPUTERNAME_LENGTH</b> + 1 
       characters. On output, <i>pcchNetName</i> points to the actual number of characters copied 
       to the content of <i>lpszNetName</i>.

## -returns

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The resource indexed by <i>lObjIndex</i> has a 
         <a href="/previous-versions/windows/desktop/mscs/resource-dependencies">dependency</a> on a 
         <a href="/previous-versions/windows/desktop/mscs/network-name">Network Name</a> resource, and the name of the 
         network was successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The resource indexed by <i>lObjIndex</i> does not have a dependency on a Network Name 
         resource.

</td>
</tr>
</table>

## -remarks

The 
     <b>GetResourceNetworkName</b> 
     method is necessary to allow 
     <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> extension property 
     pages to determine whether a resource has an existing or a pending dependency on a Network Name resource.

The name of the network is stored in the Network Name resource's Name private property. The Network Name 
     resource's Name common property is the name of the resource, not the network.

<b>MAX_COMPUTERNAME_LENGTH</b> is a constant defined as 15 in the Windows header file 
     WinBase.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusterdatainfo-getobjectcount">IGetClusterDataInfo::GetObjectCount</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterresourceinfo">IGetClusterResourceInfo</a>
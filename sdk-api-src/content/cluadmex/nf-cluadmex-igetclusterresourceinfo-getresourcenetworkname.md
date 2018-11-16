---
UID: NF:cluadmex.IGetClusterResourceInfo.GetResourceNetworkName
title: IGetClusterResourceInfo::GetResourceNetworkName
author: windows-sdk-content
description: Returns the name of the network managed by the Network Name resource on which a resource depends.
old-location: mscs\igetclusterresourceinfo_getresourcenetworkname.htm
tech.root: MsCS
ms.assetid: 5c4a16ab-b71c-49f6-95cb-8627eaffb8d6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetResourceNetworkName, GetResourceNetworkName method [Failover Cluster], GetResourceNetworkName method [Failover Cluster],IGetClusterResourceInfo interface, IGetClusterResourceInfo interface [Failover Cluster],GetResourceNetworkName method, IGetClusterResourceInfo.GetResourceNetworkName, IGetClusterResourceInfo::GetResourceNetworkName, _wolf_igetclusterresourceinfo_getresourcenetworkname, cluadmex/IGetClusterResourceInfo::GetResourceNetworkName, mscs.igetclusterresourceinfo_getresourcenetworkname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cluadmex.h
api_name:
 - IGetClusterResourceInfo.GetResourceNetworkName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- cluadmex.h
: 
- IGetClusterResourceInfo.GetResourceNetworkName
: 
---

# IGetClusterResourceInfo::GetResourceNetworkName


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns the name of the <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a> managed by the 
    <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">Network Name</a> resource on which a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> depends.


## -parameters




### -param lObjIndex [in]

A number representing the zero-based index of the target resource. The target resource may or may not depend 
       on a Network Name resource. <i>lObjIndex</i> is restricted to the number that can be 
       retrieved by calling 
       <a href="https://msdn.microsoft.com/20ef63e2-bcec-48bc-86e8-ab746fb72cc5">IGetClusterDataInfo::GetObjectCount</a>.


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
         <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependency</a> on a 
         <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">Network Name</a> resource, and the name of the 
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
     <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> extension property 
     pages to determine whether a resource has an existing or a pending dependency on a Network Name resource.

The name of the network is stored in the Network Name resource's Name private property. The Network Name 
     resource's Name common property is the name of the resource, not the network.

<b>MAX_COMPUTERNAME_LENGTH</b> is a constant defined as 15 in the Windows header file 
     WinBase.h.




## -see-also




<a href="https://msdn.microsoft.com/20ef63e2-bcec-48bc-86e8-ab746fb72cc5">IGetClusterDataInfo::GetObjectCount</a>



<a href="https://msdn.microsoft.com/8a3a9e9d-4666-4d9a-83e3-10d667b42d66">IGetClusterResourceInfo</a>
 

 


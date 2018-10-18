---
UID: NF:cluadmex.IGetClusterResourceInfo.GetResourceNetworkName
title: IGetClusterResourceInfo::GetResourceNetworkName
author: windows-sdk-content
description: Returns the name of the network managed by the Network Name resource on which a resource depends.
old-location: mscs\igetclusterresourceinfo_getresourcenetworkname.htm
tech.root: mscs
ms.assetid: 5c4a16ab-b71c-49f6-95cb-8627eaffb8d6
ms.author: windowssdkdev
ms.date: 10/12/2018
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
---

# IGetClusterResourceInfo::GetResourceNetworkName


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns the name of the <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">network</a> managed by the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa371733(v=VS.85).aspx">Network Name</a> resource on which a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a> depends.


## -parameters




### -param lObjIndex [in]

A number representing the zero-based index of the target resource. The target resource may or may not depend 
       on a Network Name resource. <i>lObjIndex</i> is restricted to the number that can be 
       retrieved by calling 
       <a href="https://msdn.microsoft.com/en-us/library/Aa370214(v=VS.85).aspx">IGetClusterDataInfo::GetObjectCount</a>.


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



This method returns BOOL.




## -remarks



The 
     <b>GetResourceNetworkName</b> 
     method is necessary to allow 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369060(v=VS.85).aspx">Failover Cluster Administrator</a> extension property 
     pages to determine whether a resource has an existing or a pending dependency on a Network Name resource.

The name of the network is stored in the Network Name resource's Name private property. The Network Name 
     resource's Name common property is the name of the resource, not the network.

<b>MAX_COMPUTERNAME_LENGTH</b> is a constant defined as 15 in the Windows header file 
     WinBase.h.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa370214(v=VS.85).aspx">IGetClusterDataInfo::GetObjectCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370230(v=VS.85).aspx">IGetClusterResourceInfo</a>
 

 


---
UID: NF:cluadmex.IGetClusterUIInfo.GetClusterName
title: IGetClusterUIInfo::GetClusterName
author: windows-sdk-content
description: Returns the name of the cluster.
old-location: mscs\igetclusteruiinfo_getclustername.htm
old-project: mscs
ms.assetid: 2c892250-80b7-4bf8-9514-64833d0e3450
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetClusterName, GetClusterName method [Failover Cluster], GetClusterName method [Failover Cluster],IGetClusterUIInfo interface, IGetClusterUIInfo interface [Failover Cluster],GetClusterName method, IGetClusterUIInfo.GetClusterName, IGetClusterUIInfo::GetClusterName, _wolf_igetclusteruiinfo_getclustername, cluadmex/IGetClusterUIInfo::GetClusterName, mscs.igetclusteruiinfo_getclustername
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: cluadmex.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cluadmex.h
api_name:
 - IGetClusterUIInfo.GetClusterName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGetClusterUIInfo::GetClusterName


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns the name of the <a href="c_gly.htm">cluster</a>.


## -parameters




### -param lpszName [out]

Pointer to a null-terminated Unicode string containing the name of the cluster, or 
       <b>NULL</b> to indicate that the caller is requesting only the length of the name. Although 
       declared as a <b>BSTR</b>, this parameter is implemented as an 
       <b>LPWSTR</b>.


### -param pcchName [in, out]

On input, pointer to the count of characters in the buffer pointed to by the 
       <i>lpszName</i> parameter. On output, pointer to the total number of characters in the 
       buffer including the <b>NULL</b>-terminating character.


## -returns



If <b>GetClusterName</b> is not 
       successful, it can return other <b>HRESULT</b> values.




## -remarks



If the <i>lpszName</i> parameter is set to <b>NULL</b> and the 
     <i>pcchName</i> parameter is not set to <b>NULL</b>, the 
     <b>GetClusterName</b> method returns 
     <b>NOERROR</b>.




## -see-also




<a href="https://msdn.microsoft.com/e41afb20-5bb8-475f-a056-53d7be8f4bf0">IGetClusterUIInfo</a>
 

 


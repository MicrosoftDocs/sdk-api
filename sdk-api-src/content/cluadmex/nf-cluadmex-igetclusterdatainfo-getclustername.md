---
UID: NF:cluadmex.IGetClusterDataInfo.GetClusterName
title: IGetClusterDataInfo::GetClusterName method
author: windows-driver-content
description: Returns the name of the cluster.
old-location: mscs\igetclusterdatainfo_getclustername.htm
old-project: MsCS
ms.assetid: 711a193f-de29-4e90-adf1-6dc6e95c0c61
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: GetClusterName method [Failover Cluster], GetClusterName method [Failover Cluster], IGetClusterDataInfo interface, GetClusterName,IGetClusterDataInfo.GetClusterName, IGetClusterDataInfo, IGetClusterDataInfo interface [Failover Cluster], GetClusterName method, IGetClusterDataInfo::GetClusterName, _wolf_igetclusterdatainfo_getclustername, cluadmex/IGetClusterDataInfo::GetClusterName, mscs.igetclusterdatainfo_getclustername
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	cluadmex.h
api_name:
-	IGetClusterDataInfo.GetClusterName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGetClusterDataInfo::GetClusterName method


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns the name of the cluster.


## -parameters




### -param lpszName [out]

Pointer to a null-terminated Unicode string containing the name of the cluster; or 
       <b>NULL</b> to indicate that the caller is requesting only the length of the name. Although 
       declared as a <b>BSTR</b>, this parameter is implemented as an 
       <b>LPWSTR</b>.


### -param pcchName [in, out]

On input, pointer to the size of the buffer, in characters, pointed to by the 
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




<a href="https://msdn.microsoft.com/a2800ac8-a865-4e66-8147-90e95b54cb0c">IGetClusterDataInfo</a>
 

 


---
UID: NF:cluadmex.IGetClusterDataInfo.GetObjectCount
title: IGetClusterDataInfo::GetObjectCount
author: windows-sdk-content
description: Returns a count of the number of selected cluster objects.
old-location: mscs\igetclusterdatainfo_getobjectcount.htm
tech.root: mscs
ms.assetid: 20ef63e2-bcec-48bc-86e8-ab746fb72cc5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetObjectCount, GetObjectCount method [Failover Cluster], GetObjectCount method [Failover Cluster],IGetClusterDataInfo interface, IGetClusterDataInfo interface [Failover Cluster],GetObjectCount method, IGetClusterDataInfo.GetObjectCount, IGetClusterDataInfo::GetObjectCount, _wolf_igetclusterdatainfo_getobjectcount, cluadmex/IGetClusterDataInfo::GetObjectCount, mscs.igetclusterdatainfo_getobjectcount
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
 - IGetClusterDataInfo.GetObjectCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGetClusterDataInfo::GetObjectCount


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns a count of the number of selected 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster objects</a>.


## -parameters






## -returns



A count of the number of selected objects.




## -remarks



Because <a href="https://msdn.microsoft.com/en-us/library/Aa369060(v=VS.85).aspx">Failover Cluster Administrator</a> supports 
     only one selected object, the 
     <b>GetObjectCount</b> method always returns 
     1.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa370211(v=VS.85).aspx">IGetClusterDataInfo</a>
 

 


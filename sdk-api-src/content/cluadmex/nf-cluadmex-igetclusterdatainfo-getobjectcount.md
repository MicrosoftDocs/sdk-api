---
UID: NF:cluadmex.IGetClusterDataInfo.GetObjectCount
title: IGetClusterDataInfo::GetObjectCount (cluadmex.h)
author: windows-sdk-content
description: Returns a count of the number of selected cluster objects.
old-location: mscs\igetclusterdatainfo_getobjectcount.htm
tech.root: MsCS
ms.assetid: 20ef63e2-bcec-48bc-86e8-ab746fb72cc5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetObjectCount, GetObjectCount method [Failover Cluster], GetObjectCount method [Failover Cluster],IGetClusterDataInfo interface, IGetClusterDataInfo interface [Failover Cluster],GetObjectCount method, IGetClusterDataInfo.GetObjectCount, IGetClusterDataInfo::GetObjectCount, _wolf_igetclusterdatainfo_getobjectcount, cluadmex/IGetClusterDataInfo::GetObjectCount, mscs.igetclusterdatainfo_getobjectcount
ms.topic: method
f1_keywords: ["cluadmex/IGetClusterDataInfo.GetObjectCount"]
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
ms.custom: 19H1
---

# IGetClusterDataInfo::GetObjectCount


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns a count of the number of selected 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-objects">cluster objects</a>.


## -parameters






## -returns



A count of the number of selected objects.




## -remarks



Because <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> supports 
     only one selected object, the 
     <b>GetObjectCount</b> method always returns 
     1.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterdatainfo">IGetClusterDataInfo</a>
 

 


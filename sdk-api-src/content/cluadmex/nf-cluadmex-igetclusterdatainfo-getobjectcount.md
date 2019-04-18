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
    <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster objects</a>.


## -parameters






## -returns



A count of the number of selected objects.




## -remarks



Because <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> supports 
     only one selected object, the 
     <b>GetObjectCount</b> method always returns 
     1.




## -see-also




<a href="https://msdn.microsoft.com/a2800ac8-a865-4e66-8147-90e95b54cb0c">IGetClusterDataInfo</a>
 

 


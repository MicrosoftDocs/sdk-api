---
UID: NS:clusapi._FILESHARE_CHANGE_LIST
title: FILESHARE_CHANGE_LIST (clusapi.h)
author: windows-sdk-content
description: Describes an event notification list for file shares managed by the File Server resource.
old-location: mscs\fileshare_change_list.htm
tech.root: MsCS
ms.assetid: 7bc77f09-8984-497c-9d86-d8e8d4b55b94
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PFILESHARE_CHANGE_LIST, FILESHARE_CHANGE_LIST, FILESHARE_CHANGE_LIST structure [Failover Cluster], PFILESHARE_CHANGE_LIST, PFILESHARE_CHANGE_LIST structure pointer [Failover Cluster], clusapi/FILESHARE_CHANGE_LIST, clusapi/PFILESHARE_CHANGE_LIST, mscs.fileshare_change_list'
ms.topic: struct
f1_keywords:
- clusapi/FILESHARE_CHANGE_LIST
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
- HeaderDef
api_location:
- ClusAPI.h
api_name:
- FILESHARE_CHANGE_LIST
product: Windows
targetos: Windows
req.typenames: FILESHARE_CHANGE_LIST, *PFILESHARE_CHANGE_LIST
req.redist: 
ms.custom: 19H1
---

# FILESHARE_CHANGE_LIST structure


## -description


Describes an event notification list for file shares managed by the File Server 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resources">resource</a>.


## -struct-fields




### -field NumEntries

The number of entries the event notification list contains.


### -field ChangeEntry

An entry in the event notification list. The format of this member comes from the 
       <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/ns-clusapi-fileshare_change">FILESHARE_CHANGE</a> structure.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/ns-clusapi-fileshare_change">FILESHARE_CHANGE</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/utility-structures">Utility Structures</a>
 

 


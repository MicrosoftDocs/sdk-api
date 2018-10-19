---
UID: NS:clusapi._FILESHARE_CHANGE
title: "_FILESHARE_CHANGE"
author: windows-sdk-content
description: Describes the format for an entry in an event notification list.
old-location: mscs\fileshare_change.htm
tech.root: mscs
ms.assetid: f317f162-49b2-43df-a298-e2de707e089a
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PFILESHARE_CHANGE, FILESHARE_CHANGE, FILESHARE_CHANGE structure [Failover Cluster], FILESHARE_CHANGE_ADD, FILESHARE_CHANGE_DEL, FILESHARE_CHANGE_MODIFY, PFILESHARE_CHANGE, PFILESHARE_CHANGE structure pointer [Failover Cluster], _FILESHARE_CHANGE, clusapi/FILESHARE_CHANGE, clusapi/PFILESHARE_CHANGE, mscs.fileshare_change"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - FILESHARE_CHANGE
product: Windows
targetos: Windows
req.typenames: FILESHARE_CHANGE, *PFILESHARE_CHANGE
req.redist: 
---

# _FILESHARE_CHANGE structure


## -description


Describes the format for an entry in an event notification list.


## -struct-fields




### -field Change

Describes a change event. This value is taken from the 
       <a href="https://msdn.microsoft.com/36139a95-141c-4f44-9627-9ed6c3fed0c5">FILESHARE_CHANGE_ENUM</a>enumeration. The following 
       are the possible values for this member.



#### FILESHARE_CHANGE_ADD (1)

A new file share resource has been created and will be included with the other file shares managed by the 
         File Server resource.



#### FILESHARE_CHANGE_DEL (2)

A file share resource has been deleted and will be removed from the file shares managed by the File Server 
         resource.



#### FILESHARE_CHANGE_MODIFY (3)

One or more properties of an existing file share resource have been changed.


### -field ShareName

The name of the file share resource specific to this entry in the event notification list.


## -see-also




<a href="https://msdn.microsoft.com/36139a95-141c-4f44-9627-9ed6c3fed0c5">FILESHARE_CHANGE_ENUM</a>



<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility Structures</a>
 

 


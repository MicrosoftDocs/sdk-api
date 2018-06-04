---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DiskQuotaUserInformation structure


## -description


Represents the per-user quota information.


## -struct-fields




### -field QuotaUsed

The disk space charged to the user, in bytes. This is the amount of information stored, not necessarily the number of bytes used on disk.


### -field QuotaThreshold

The warning threshold for the user, in bytes. You can use the 
<a href="https://msdn.microsoft.com/8e5a1637-ad10-4a36-8493-b57c254ae273">IDiskQuotaControl::SetQuotaLogFlags</a> method to configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value.


### -field QuotaLimit

The quota limit for the user, in bytes. If this value is -1, the user has an unlimited quota. 




You can use the <a href="https://msdn.microsoft.com/8e5a1637-ad10-4a36-8493-b57c254ae273">IDiskQuotaControl::SetQuotaLogFlags</a> method to configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value. You can also use the 
<a href="https://msdn.microsoft.com/0bbacc3c-e212-4801-95d8-1e260123665d">IDiskQuotaControl::SetQuotaState</a> method to configure the system to deny additional disk space to the user when the disk space charged to the user exceeds this value.


## -see-also




<a href="https://msdn.microsoft.com/8e5a1637-ad10-4a36-8493-b57c254ae273">IDiskQuotaControl::SetQuotaLogFlags</a>



<a href="https://msdn.microsoft.com/0bbacc3c-e212-4801-95d8-1e260123665d">IDiskQuotaControl::SetQuotaState</a>



<a href="https://msdn.microsoft.com/d1640803-965a-473c-bf10-bee51d47fcfa">IDiskQuotaUser::GetQuotaInformation</a>
 

 


---
UID: NS:dskquota.DiskQuotaUserInformation
title: DiskQuotaUserInformation
author: windows-sdk-content
description: Represents the per-user quota information.
old-location: fs\diskquota_user_information_str.htm
tech.root: fileio
ms.assetid: 8929faab-e15e-47a0-af9e-b64684272cb7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PDISKQUOTA_USER_INFORMATION, DISKQUOTA_USER_INFORMATION, DISKQUOTA_USER_INFORMATION structure [Files], DiskQuotaUserInformation, PDISKQUOTA_USER_INFORMATION, PDISKQUOTA_USER_INFORMATION structure pointer [Files], _win32_diskquota_user_information_str, base.diskquota_user_information_str, dskquota/DISKQUOTA_USER_INFORMATION, dskquota/PDISKQUOTA_USER_INFORMATION, fs.diskquota_user_information_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dskquota.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Dskquota.h
api_name:
 - DISKQUOTA_USER_INFORMATION
product: Windows
targetos: Windows
req.typenames: DISKQUOTA_USER_INFORMATION, *PDISKQUOTA_USER_INFORMATION
req.redist: 
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
 

 


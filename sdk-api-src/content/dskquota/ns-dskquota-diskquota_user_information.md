---
UID: NS:dskquota.DiskQuotaUserInformation
title: DISKQUOTA_USER_INFORMATION (dskquota.h)
description: Represents the per-user quota information.
helpviewer_keywords: ["*PDISKQUOTA_USER_INFORMATION","DISKQUOTA_USER_INFORMATION","DISKQUOTA_USER_INFORMATION structure [Files]","PDISKQUOTA_USER_INFORMATION","PDISKQUOTA_USER_INFORMATION structure pointer [Files]","_win32_diskquota_user_information_str","base.diskquota_user_information_str","dskquota/DISKQUOTA_USER_INFORMATION","dskquota/PDISKQUOTA_USER_INFORMATION","fs.diskquota_user_information_str"]
old-location: fs\diskquota_user_information_str.htm
tech.root: fs
ms.assetid: 8929faab-e15e-47a0-af9e-b64684272cb7
ms.date: 12/05/2018
ms.keywords: '*PDISKQUOTA_USER_INFORMATION, DISKQUOTA_USER_INFORMATION, DISKQUOTA_USER_INFORMATION structure [Files], PDISKQUOTA_USER_INFORMATION, PDISKQUOTA_USER_INFORMATION structure pointer [Files], _win32_diskquota_user_information_str, base.diskquota_user_information_str, dskquota/DISKQUOTA_USER_INFORMATION, dskquota/PDISKQUOTA_USER_INFORMATION, fs.diskquota_user_information_str'
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
targetos: Windows
req.typenames: DISKQUOTA_USER_INFORMATION, *PDISKQUOTA_USER_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DiskQuotaUserInformation
 - dskquota/DiskQuotaUserInformation
 - PDISKQUOTA_USER_INFORMATION
 - dskquota/PDISKQUOTA_USER_INFORMATION
 - DISKQUOTA_USER_INFORMATION
 - dskquota/DISKQUOTA_USER_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dskquota.h
api_name:
 - DISKQUOTA_USER_INFORMATION
---

# DISKQUOTA_USER_INFORMATION structure


## -description

Represents the per-user quota information.

## -struct-fields

### -field QuotaUsed

The disk space charged to the user, in bytes. This is the amount of information stored, not necessarily the number of bytes used on disk.

### -field QuotaThreshold

The warning threshold for the user, in bytes. You can use the 
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-setquotalogflags">IDiskQuotaControl::SetQuotaLogFlags</a> method to configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value.

### -field QuotaLimit

The quota limit for the user, in bytes. If this value is -1, the user has an unlimited quota. 




You can use the <a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-setquotalogflags">IDiskQuotaControl::SetQuotaLogFlags</a> method to configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value. You can also use the 
<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-setquotastate">IDiskQuotaControl::SetQuotaState</a> method to configure the system to deny additional disk space to the user when the disk space charged to the user exceeds this value.

## -see-also

<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-setquotalogflags">IDiskQuotaControl::SetQuotaLogFlags</a>



<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotacontrol-setquotastate">IDiskQuotaControl::SetQuotaState</a>



<a href="/windows/desktop/api/dskquota/nf-dskquota-idiskquotauser-getquotainformation">IDiskQuotaUser::GetQuotaInformation</a>
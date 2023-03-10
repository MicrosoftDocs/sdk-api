---
UID: NE:bits.BG_JOB_TYPE
title: BG_JOB_TYPE (bits.h)
description: Defines constants that specify the type of transfer job, such as download.
helpviewer_keywords: ["BG_JOB_TYPE","BG_JOB_TYPE enumeration [BITS]","BG_JOB_TYPE_DOWNLOAD","BG_JOB_TYPE_UPLOAD","BG_JOB_TYPE_UPLOAD_REPLY","_drz_bg_job_type","bits.bg_job_type","bits/BG_JOB_TYPE","bits/BG_JOB_TYPE_DOWNLOAD","bits/BG_JOB_TYPE_UPLOAD","bits/BG_JOB_TYPE_UPLOAD_REPLY"]
old-location: bits\bg_job_type.htm
tech.root: Bits
ms.assetid: b341a63f-3a1d-4518-8f05-17d28af603b4
ms.date: 02/20/2019
ms.keywords: BG_JOB_TYPE, BG_JOB_TYPE enumeration [BITS], BG_JOB_TYPE_DOWNLOAD, BG_JOB_TYPE_UPLOAD, BG_JOB_TYPE_UPLOAD_REPLY, _drz_bg_job_type, bits.bg_job_type, bits/BG_JOB_TYPE, bits/BG_JOB_TYPE_DOWNLOAD, bits/BG_JOB_TYPE_UPLOAD, bits/BG_JOB_TYPE_UPLOAD_REPLY
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.typenames: BG_JOB_TYPE
req.redist: 
f1_keywords:
 - BG_JOB_TYPE
 - bits/BG_JOB_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits.h
api_name:
 - BG_JOB_TYPE
---

# BG_JOB_TYPE enumeration


## -description

Defines constants that specify the type of transfer job, such as download.

## -enum-fields

### -field BG_JOB_TYPE_DOWNLOAD:0

Specifies that the job downloads files to the client.

### -field BG_JOB_TYPE_UPLOAD

Specifies that the job uploads a file to the server. 

**BITS 1.2 and earlier:** not supported.

### -field BG_JOB_TYPE_UPLOAD_REPLY

Specifies that the job uploads a file to the server, and receives a reply file from the server application. 

**BITS 1.2 and earlier:** not supported.

## -see-also

* [IBackgroundCopyJob::GetType method](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-gettype)
* [IBackgroundCopyManager::CreateJob method](/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-createjob)


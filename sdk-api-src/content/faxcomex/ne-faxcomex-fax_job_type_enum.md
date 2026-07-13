---
UID: NE:faxcomex.FAX_JOB_TYPE_ENUM
title: FAX_JOB_TYPE_ENUM (faxcomex.h)
description: The FAX_JOB_TYPE_ENUM enumeration defines the fax job type.
helpviewer_keywords: ["FAX_JOB_TYPE_ENUM","FAX_JOB_TYPE_ENUM enumeration [Fax Service]","_mfax_fax_job_type_enum","fax._mfax_fax_job_type_enum","faxcomex/FAX_JOB_TYPE_ENUM","faxcomex/fjtRECEIVE","faxcomex/fjtROUTING","faxcomex/fjtSEND","fjtRECEIVE","fjtROUTING","fjtSEND"]
old-location: fax\_mfax_fax_job_type_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_5jql.htm
ms.date: 12/05/2018
ms.keywords: FAX_JOB_TYPE_ENUM, FAX_JOB_TYPE_ENUM enumeration [Fax Service], _mfax_fax_job_type_enum, fax._mfax_fax_job_type_enum, faxcomex/FAX_JOB_TYPE_ENUM, faxcomex/fjtRECEIVE, faxcomex/fjtROUTING, faxcomex/fjtSEND, fjtRECEIVE, fjtROUTING, fjtSEND
req.header: faxcomex.h
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
req.typenames: FAX_JOB_TYPE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FAX_JOB_TYPE_ENUM
 - faxcomex/FAX_JOB_TYPE_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_JOB_TYPE_ENUM
---

# FAX_JOB_TYPE_ENUM enumeration


## -description

The <b>FAX_JOB_TYPE_ENUM</b> enumeration defines the fax job type.

## -enum-fields

### -field fjtSEND:0

The job is an outbound job.

### -field fjtRECEIVE

The job is an incoming job (being received through a modem).

### -field fjtROUTING

The incoming job has been received, and is now in routing mode (modem is not used).

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxjobstatus-jobtype-vb">IFaxJobStatus::get_JobType</a>

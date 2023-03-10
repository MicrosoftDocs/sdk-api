---
UID: NE:faxcomex.FAX_JOB_OPERATIONS_ENUM
title: FAX_JOB_OPERATIONS_ENUM (faxcomex.h)
description: The FAX_JOB_OPERATIONS_ENUM enumeration defines the operations that can be performed on a fax job. The members of this enumeration are bit values and can be used in combination.
helpviewer_keywords: ["FAX_JOB_OPERATIONS_ENUM","FAX_JOB_OPERATIONS_ENUM enumeration [Fax Service]","_mfax_fax_job_operations_enum","fax._mfax_fax_job_operations_enum","faxcomex/FAX_JOB_OPERATIONS_ENUM","faxcomex/fjoDELETE","faxcomex/fjoPAUSE","faxcomex/fjoRECIPIENT_INFO","faxcomex/fjoRESTART","faxcomex/fjoRESUME","faxcomex/fjoSENDER_INFO","faxcomex/fjoVIEW","fjoDELETE","fjoPAUSE","fjoRECIPIENT_INFO","fjoRESTART","fjoRESUME","fjoSENDER_INFO","fjoVIEW"]
old-location: fax\_mfax_fax_job_operations_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_1ijx.htm
ms.date: 12/05/2018
ms.keywords: FAX_JOB_OPERATIONS_ENUM, FAX_JOB_OPERATIONS_ENUM enumeration [Fax Service], _mfax_fax_job_operations_enum, fax._mfax_fax_job_operations_enum, faxcomex/FAX_JOB_OPERATIONS_ENUM, faxcomex/fjoDELETE, faxcomex/fjoPAUSE, faxcomex/fjoRECIPIENT_INFO, faxcomex/fjoRESTART, faxcomex/fjoRESUME, faxcomex/fjoSENDER_INFO, faxcomex/fjoVIEW, fjoDELETE, fjoPAUSE, fjoRECIPIENT_INFO, fjoRESTART, fjoRESUME, fjoSENDER_INFO, fjoVIEW
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
req.typenames: FAX_JOB_OPERATIONS_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FAX_JOB_OPERATIONS_ENUM
 - faxcomex/FAX_JOB_OPERATIONS_ENUM
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
 - FAX_JOB_OPERATIONS_ENUM
---

# FAX_JOB_OPERATIONS_ENUM enumeration


## -description

The <b>FAX_JOB_OPERATIONS_ENUM</b> enumeration defines the operations that can be performed on a fax job. The members of this enumeration are bit values and can be used in combination.

## -enum-fields

### -field fjoVIEW:0x1

The job's TIFF image can be retrieved.

### -field fjoPAUSE:0x2

The job can be paused.

### -field fjoRESUME:0x4

The job can be resumed.

### -field fjoRESTART:0x8

The job can be restarted.

### -field fjoDELETE:0x10

The job can be deleted.

### -field fjoRECIPIENT_INFO:0x20

The job's recipient information can be retrieved.

### -field fjoSENDER_INFO:0x40

The job's sender information can be retrieved.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-availableoperations">AvailableOperations</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxjobstatus-availableoperations-vb">IFaxJobStatus::get_AvailableOperations</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-availableoperations-vb">IFaxOutgoingJob::get_AvailableOperations</a>

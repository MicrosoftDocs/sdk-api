---
UID: NE:faxcomex.FAX_JOB_OPERATIONS_ENUM
title: FAX_JOB_OPERATIONS_ENUM
author: windows-sdk-content
description: The FAX_JOB_OPERATIONS_ENUM enumeration defines the operations that can be performed on a fax job. The members of this enumeration are bit values and can be used in combination.
old-location: fax\_mfax_fax_job_operations_enum.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_1ijx.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: FAX_JOB_OPERATIONS_ENUM, FAX_JOB_OPERATIONS_ENUM enumeration [Fax Service], _mfax_fax_job_operations_enum, fax._mfax_fax_job_operations_enum, faxcomex/FAX_JOB_OPERATIONS_ENUM, faxcomex/fjoDELETE, faxcomex/fjoPAUSE, faxcomex/fjoRECIPIENT_INFO, faxcomex/fjoRESTART, faxcomex/fjoRESUME, faxcomex/fjoSENDER_INFO, faxcomex/fjoVIEW, fjoDELETE, fjoPAUSE, fjoRECIPIENT_INFO, fjoRESTART, fjoRESUME, fjoSENDER_INFO, fjoVIEW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: FAX_JOB_OPERATIONS_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_JOB_OPERATIONS_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# FAX_JOB_OPERATIONS_ENUM enumeration


## -description


The <b>FAX_JOB_OPERATIONS_ENUM</b> enumeration defines the operations that can be performed on a fax job. The members of this enumeration are bit values and can be used in combination.


## -enum-fields




### -field fjoVIEW

The job's TIFF image can be retrieved.


### -field fjoPAUSE

The job can be paused.


### -field fjoRESUME

The job can be resumed.


### -field fjoRESTART

The job can be restarted.


### -field fjoDELETE

The job can be deleted.


### -field fjoRECIPIENT_INFO

The job's recipient information can be retrieved.


### -field fjoSENDER_INFO

The job's sender information can be retrieved.


## -see-also




<a href="https://msdn.microsoft.com/library/ms684593(v=VS.85).aspx">AvailableOperations</a>



<a href="https://msdn.microsoft.com/library/ms684920(v=VS.85).aspx">IFaxJobStatus::get_AvailableOperations</a>



<a href="https://msdn.microsoft.com/library/ms690257(v=VS.85).aspx">IFaxOutgoingJob::get_AvailableOperations</a>
 

 


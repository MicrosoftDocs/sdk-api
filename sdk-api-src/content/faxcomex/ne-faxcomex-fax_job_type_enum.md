---
UID: NE:faxcomex.FAX_JOB_TYPE_ENUM
title: FAX_JOB_TYPE_ENUM
author: windows-sdk-content
description: The FAX_JOB_TYPE_ENUM enumeration defines the fax job type.
old-location: fax\_mfax_fax_job_type_enum.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_5jql.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FAX_JOB_TYPE_ENUM, FAX_JOB_TYPE_ENUM enumeration [Fax Service], _mfax_fax_job_type_enum, fax._mfax_fax_job_type_enum, faxcomex/FAX_JOB_TYPE_ENUM, faxcomex/fjtRECEIVE, faxcomex/fjtROUTING, faxcomex/fjtSEND, fjtRECEIVE, fjtROUTING, fjtSEND
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
req.typenames: FAX_JOB_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxComex.h
api_name:
 - FAX_JOB_TYPE_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# FAX_JOB_TYPE_ENUM enumeration


## -description


The <b>FAX_JOB_TYPE_ENUM</b> enumeration defines the fax job type.


## -enum-fields




### -field fjtSEND

The job is an outbound job.


### -field fjtRECEIVE

The job is an incoming job (being received through a modem).


### -field fjtROUTING

The incoming job has been received, and is now in routing mode (modem is not used). 


## -see-also




<a href="https://msdn.microsoft.com/30e91faa-7682-411c-b57d-b4d2823f47b0">IFaxJobStatus::get_JobType</a>
 

 


---
UID: NE:faxcomex.FAX_JOB_STATUS_ENUM
title: FAX_JOB_STATUS_ENUM (faxcomex.h)
description: The FAX_JOB_STATUS_ENUM enumeration defines the status values for a fax job.Note  The members fjsPAUSED and fjsNOLINE are modifiers; they can be used in combination with any other member of this enumeration.helpviewer_keywords: ["FAX_JOB_STATUS_ENUM","FAX_JOB_STATUS_ENUM enumeration [Fax Service]","_mfax_fax_job_status_enum","fax._mfax_fax_job_status_enum","faxcomex/FAX_JOB_STATUS_ENUM","faxcomex/fjsCANCELED","faxcomex/fjsCANCELING","faxcomex/fjsCOMPLETED","faxcomex/fjsFAILED","faxcomex/fjsINPROGRESS","faxcomex/fjsNOLINE","faxcomex/fjsPAUSED","faxcomex/fjsPENDING","faxcomex/fjsRETRIES_EXCEEDED","faxcomex/fjsRETRYING","faxcomex/fjsROUTING","fjsCANCELED","fjsCANCELING","fjsCOMPLETED","fjsFAILED","fjsINPROGRESS","fjsNOLINE","fjsPAUSED","fjsPENDING","fjsRETRIES_EXCEEDED","fjsRETRYING","fjsROUTING"]
old-location: fax\_mfax_fax_job_status_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7zcd.htm
ms.date: 12/05/2018
ms.keywords: FAX_JOB_STATUS_ENUM, FAX_JOB_STATUS_ENUM enumeration [Fax Service], _mfax_fax_job_status_enum, fax._mfax_fax_job_status_enum, faxcomex/FAX_JOB_STATUS_ENUM, faxcomex/fjsCANCELED, faxcomex/fjsCANCELING, faxcomex/fjsCOMPLETED, faxcomex/fjsFAILED, faxcomex/fjsINPROGRESS, faxcomex/fjsNOLINE, faxcomex/fjsPAUSED, faxcomex/fjsPENDING, faxcomex/fjsRETRIES_EXCEEDED, faxcomex/fjsRETRYING, faxcomex/fjsROUTING, fjsCANCELED, fjsCANCELING, fjsCOMPLETED, fjsFAILED, fjsINPROGRESS, fjsNOLINE, fjsPAUSED, fjsPENDING, fjsRETRIES_EXCEEDED, fjsRETRYING, fjsROUTING
f1_keywords:
- faxcomex/FAX_JOB_STATUS_ENUM
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- FaxComex.h
api_name:
- FAX_JOB_STATUS_ENUM
targetos: Windows
req.typenames: FAX_JOB_STATUS_ENUM
req.redist: 
ms.custom: 19H1
---

# FAX_JOB_STATUS_ENUM enumeration


## -description


The <b>FAX_JOB_STATUS_ENUM</b> enumeration defines the status values for a fax job.
<div class="alert"><b>Note</b>  The members <b><b>fjsPAUSED</b></b> and <b><b>fjsNOLINE</b></b> are modifiers; they can be used in combination with any other member of this enumeration. Other members cannot be used as modifiers.</div><div> </div>

## -enum-fields




### -field fjsPENDING

The fax job is in the queue and pending service.


### -field fjsINPROGRESS

The fax job is in progress.


### -field fjsFAILED

The fax job failed.


### -field fjsPAUSED

The fax server paused the fax job. This value can arrive in a bitwise combination with another value.


### -field fjsNOLINE

There is no line available to send the fax. The fax server will send the transmission when a line is available. This value can arrive in a bitwise combination with another value.


### -field fjsRETRYING

The fax job failed. The fax server will attempt to retransmit the fax after a specified interval.


### -field fjsRETRIES_EXCEEDED

The fax server exceeded the maximum number of retransmission attempts allowed. The fax will not be sent.


### -field fjsCOMPLETED

The fax job is completed.


### -field fjsCANCELED

The fax job was canceled.


### -field fjsCANCELING

The fax job is being canceled.


### -field fjsROUTING

The fax job is being routed.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxjobstatus-status-vb">IFaxJobStatus::get_Status</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingjob-status-vb">IFaxOutgoingJob::get_Status</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxincomingjob-status">Status</a>
 

 


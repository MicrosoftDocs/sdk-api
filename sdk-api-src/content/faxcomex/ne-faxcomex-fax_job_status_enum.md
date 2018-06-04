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




<a href="https://msdn.microsoft.com/114ad232-1213-4af8-857f-5e32556c0330">IFaxJobStatus::get_Status</a>



<a href="https://msdn.microsoft.com/90553615-ded2-4e4c-9411-a513fd682423">IFaxOutgoingJob::get_Status</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a>
 

 


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

# _VSS_APPLICATION_LEVEL enumeration


## -description


The <b>VSS_APPLICATION_LEVEL</b> enumeration indicates 
    the application level, the point in the course of the creation of a shadow copy that a writer is notified of a 
    freeze.

VSS first sends a <a href="vssgloss_f.htm">Freeze</a> event to writers 
    initialized with <b>VSS_APP_FRONT_END</b> (called front-end level applications), then to 
    writers initialized with <b>VSS_APP_BACK_END</b> (called back-end level applications), and 
    finally to writers initialized with <b>VSS_APP_SYSTEM</b> (called system-level 
    applications).


## -enum-fields




### -field VSS_APP_UNKNOWN

The level at which this writer's freeze state will occur is not known. This indicates an application 
      error.


### -field VSS_APP_SYSTEM

This writer freeze state will occur at the system application level.


### -field VSS_APP_BACK_END

This writer freeze state will occur at the back-end application level.


### -field VSS_APP_FRONT_END

This writer freeze state will occur at the front-end application level.


### -field VSS_APP_SYSTEM_RM


### -field VSS_APP_AUTO

This writer freeze state will be determined automatically. This enumeration value is reserved for future 
      use.


## -remarks



<b>VSS_APPLICATION_LEVEL</b> is provided to allow 
    application developers to control at what point a writer will receive a Freeze event. This may be important if one 
    writer uses or depends on another writer.

For instance, if an application <i>X</i> is storing data using application 
    <i>Y</i> as an intermediate layer (for example, if <i>Y</i> implements a 
    database used by <i>X</i>), we would describe <i>X</i> as a front-end 
    application, and <i>Y</i> as a back-end application.

In this example, when freezing applications that participate in a shadow copy, you would want 
    <i>X</i> (the front-end application) to suspend its writes to the database prior to freezing 
    <i>Y </i>(the back-end application), the database service itself.

The application level of a writer is set by 
    <a href="https://msdn.microsoft.com/a427ebbd-b7c4-46ba-ba16-dd601b1f956e">CVssWriter::Initialize</a> and retrieved by 
    <a href="https://msdn.microsoft.com/09540f57-832a-49ca-9b64-e7660b331192">CVssWriter::GetCurrentLevel</a>.




## -see-also




<a href="https://msdn.microsoft.com/09540f57-832a-49ca-9b64-e7660b331192">CVssWriter::GetCurrentLevel</a>



<a href="https://msdn.microsoft.com/a427ebbd-b7c4-46ba-ba16-dd601b1f956e">CVssWriter::Initialize</a>
 

 


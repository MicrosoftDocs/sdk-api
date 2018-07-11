---
UID: NE:vss._VSS_APPLICATION_LEVEL
title: "_VSS_APPLICATION_LEVEL"
author: windows-sdk-content
description: Indicates the application level, the point in the course of the creation of a shadow copy that a writer is notified of a freeze.
old-location: base\vss_application_level.htm
old-project: vss
ms.assetid: fc7fbaee-d223-4557-987d-2c09f3877ec2
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: "*PVSS_APPLICATION_LEVEL, PVSS_APPLICATION_LEVEL, PVSS_APPLICATION_LEVEL enumeration pointer [VSS], VSS_APPLICATION_LEVEL, VSS_APPLICATION_LEVEL enumeration [VSS], VSS_APP_AUTO, VSS_APP_BACK_END, VSS_APP_FRONT_END, VSS_APP_SYSTEM, VSS_APP_UNKNOWN, _VSS_APPLICATION_LEVEL, _win32_vss_application_level, base.vss_application_level, vss/PVSS_APPLICATION_LEVEL, vss/VSS_APPLICATION_LEVEL, vss/VSS_APP_AUTO, vss/VSS_APP_BACK_END, vss/VSS_APP_FRONT_END, vss/VSS_APP_SYSTEM, vss/VSS_APP_UNKNOWN"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vss.h
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
req.typenames: VSS_APPLICATION_LEVEL, *PVSS_APPLICATION_LEVEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vss.h
api_name:
 - VSS_APPLICATION_LEVEL
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
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
 

 


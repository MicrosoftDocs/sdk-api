---
UID: NE:vss._VSS_APPLICATION_LEVEL
title: VSS_APPLICATION_LEVEL (vss.h)
description: Indicates the application level, the point in the course of the creation of a shadow copy that a writer is notified of a freeze.
helpviewer_keywords: ["*PVSS_APPLICATION_LEVEL","PVSS_APPLICATION_LEVEL","PVSS_APPLICATION_LEVEL enumeration pointer [VSS]","VSS_APPLICATION_LEVEL","VSS_APPLICATION_LEVEL enumeration [VSS]","VSS_APP_AUTO","VSS_APP_BACK_END","VSS_APP_FRONT_END","VSS_APP_SYSTEM","VSS_APP_UNKNOWN","_win32_vss_application_level","base.vss_application_level","vss/PVSS_APPLICATION_LEVEL","vss/VSS_APPLICATION_LEVEL","vss/VSS_APP_AUTO","vss/VSS_APP_BACK_END","vss/VSS_APP_FRONT_END","vss/VSS_APP_SYSTEM","vss/VSS_APP_UNKNOWN"]
old-location: base\vss_application_level.htm
tech.root: base
ms.assetid: fc7fbaee-d223-4557-987d-2c09f3877ec2
ms.date: 12/05/2018
ms.keywords: '*PVSS_APPLICATION_LEVEL, PVSS_APPLICATION_LEVEL, PVSS_APPLICATION_LEVEL enumeration pointer [VSS], VSS_APPLICATION_LEVEL, VSS_APPLICATION_LEVEL enumeration [VSS], VSS_APP_AUTO, VSS_APP_BACK_END, VSS_APP_FRONT_END, VSS_APP_SYSTEM, VSS_APP_UNKNOWN, _win32_vss_application_level, base.vss_application_level, vss/PVSS_APPLICATION_LEVEL, vss/VSS_APPLICATION_LEVEL, vss/VSS_APP_AUTO, vss/VSS_APP_BACK_END, vss/VSS_APP_FRONT_END, vss/VSS_APP_SYSTEM, vss/VSS_APP_UNKNOWN'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VSS_APPLICATION_LEVEL, *PVSS_APPLICATION_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VSS_APPLICATION_LEVEL
 - vss/_VSS_APPLICATION_LEVEL
 - PVSS_APPLICATION_LEVEL
 - vss/PVSS_APPLICATION_LEVEL
 - VSS_APPLICATION_LEVEL
 - vss/VSS_APPLICATION_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vss.h
api_name:
 - VSS_APPLICATION_LEVEL
---

# VSS_APPLICATION_LEVEL enumeration


## -description

The <b>VSS_APPLICATION_LEVEL</b> enumeration indicates 
    the application level, the point in the course of the creation of a shadow copy that a writer is notified of a 
    freeze.

VSS first sends a <a href="/windows/desktop/VSS/vssgloss-f">Freeze</a> event to writers 
    initialized with <b>VSS_APP_FRONT_END</b> (called front-end level applications), then to 
    writers initialized with <b>VSS_APP_BACK_END</b> (called back-end level applications), and 
    finally to writers initialized with <b>VSS_APP_SYSTEM</b> (called system-level 
    applications).

## -enum-fields

### -field VSS_APP_UNKNOWN:0

The level at which this writer's freeze state will occur is not known. This indicates an application 
      error.

### -field VSS_APP_SYSTEM:1

This writer freeze state will occur at the system application level.

### -field VSS_APP_BACK_END:2

This writer freeze state will occur at the back-end application level.

### -field VSS_APP_FRONT_END:3

This writer freeze state will occur at the front-end application level.

### -field VSS_APP_SYSTEM_RM:4

### -field VSS_APP_AUTO:-1

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
    <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a> and retrieved by 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-getcurrentlevel">CVssWriter::GetCurrentLevel</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-getcurrentlevel">CVssWriter::GetCurrentLevel</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a>

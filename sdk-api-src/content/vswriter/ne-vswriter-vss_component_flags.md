---
UID: NE:vswriter.VSS_COMPONENT_FLAGS
title: VSS_COMPONENT_FLAGS
author: windows-sdk-content
description: Used by writers to indicate support for auto-recovery.
old-location: base\vss_component_flags.htm
tech.root: vss
ms.assetid: 91b7fbab-82f8-48cc-8078-f8f71c48a70b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VSS_CF_APP_ROLLBACK_RECOVERY, VSS_CF_BACKUP_RECOVERY, VSS_CF_NOT_SYSTEM_STATE, VSS_COMPONENT_FLAGS, VSS_COMPONENT_FLAGS enumeration [VSS], _win32_vss_component_flags, base.vss_component_flags, enumeration [VSS], vswriter/VSS_CF_APP_ROLLBACK_RECOVERY, vswriter/VSS_CF_BACKUP_RECOVERY, vswriter/VSS_CF_NOT_SYSTEM_STATE, vswriter/VSS_COMPONENT_FLAGS
ms.topic: enum
req.header: vswriter.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - VsWriter.h
api_name:
 - VSS_COMPONENT_FLAGS
product: Windows
targetos: Windows
req.typenames: VSS_COMPONENT_FLAGS
req.redist: 
---

# VSS_COMPONENT_FLAGS enumeration


## -description


The <b>VSS_COMPONENT_FLAGS</b> enumeration is 
    used by writers to indicate support for 
    <a href="https://msdn.microsoft.com/en-us/library/Aa384651(v=VS.85).aspx">auto-recovery</a>. These 
    values are used in the <b>dwComponentFlags</b> member of 
    the <a href="https://msdn.microsoft.com/9723e90e-cd5e-4815-843b-8ed8632ebe45">VSS_COMPONENTINFO</a> structure and the 
    <i>dwComponentFlags</i> parameter of 
    the <a href="https://msdn.microsoft.com/fdbcbcea-d49e-49bc-9bb8-2210a9de02a4">IVssCreateWriterMetadata::AddComponent</a> method.


## -enum-fields




### -field VSS_CF_BACKUP_RECOVERY

The writer will need write access to this component after the shadow copy has been created.
      

This flag can be used together with the <b>VSS_VOLSNAP_ATTR_TRANSPORTABLE</b> value of the <a href="https://msdn.microsoft.com/0326a81e-036c-4548-9e09-29054e51fadd">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> enumeration if the VSS hardware provider supports LUN masking.<b>Windows Vista and Windows Server 2003 with SP1:  </b>This flag is incompatible with <b>VSS_VOLSNAP_ATTR_TRANSPORTABLE</b>.



This flag is not supported for express writers.


### -field VSS_CF_APP_ROLLBACK_RECOVERY

If this is a rollback shadow copy 
      (see the <b>VSS_VOLSNAP_ATTR_ROLLBACK_RECOVERY</b> value of the <a href="https://msdn.microsoft.com/0326a81e-036c-4548-9e09-29054e51fadd">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> enumeration), the writer for this 
      component will need write access to this component after the shadow copy has been created.
      

This flag can be used together with the <b>VSS_VOLSNAP_ATTR_TRANSPORTABLE</b> value of the <a href="https://msdn.microsoft.com/0326a81e-036c-4548-9e09-29054e51fadd">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> enumeration if the VSS hardware provider supports LUN masking.<b>Windows Vista and Windows Server 2003 with SP1:  </b>This flag is incompatible with <b>VSS_VOLSNAP_ATTR_TRANSPORTABLE</b>.



This flag is not supported for express writers.


### -field VSS_CF_NOT_SYSTEM_STATE

This component is not part of system state.

<b>Windows Server 2003 with SP1:  </b>This value is not supported until Windows Vista.


## -see-also




<a href="https://msdn.microsoft.com/fdbcbcea-d49e-49bc-9bb8-2210a9de02a4">IVssCreateWriterMetadata::AddComponent</a>



<a href="https://msdn.microsoft.com/3541c8bd-2712-458b-9153-1fffe6bf5688">VSS_BACKUP_SCHEMA</a>



<a href="https://msdn.microsoft.com/9723e90e-cd5e-4815-843b-8ed8632ebe45">VSS_COMPONENTINFO</a>



<a href="https://msdn.microsoft.com/31997417-d993-4f28-b108-ce1dd8239650">VSS_USAGE_TYPE</a>
 

 


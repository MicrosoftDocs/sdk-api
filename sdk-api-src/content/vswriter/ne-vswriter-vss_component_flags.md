---
UID: NE:vswriter.VSS_COMPONENT_FLAGS
title: VSS_COMPONENT_FLAGS (vswriter.h)
author: windows-sdk-content
description: Used by writers to indicate support for auto-recovery.
old-location: base\vss_component_flags.htm
tech.root: VSS
ms.assetid: 91b7fbab-82f8-48cc-8078-f8f71c48a70b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VSS_CF_APP_ROLLBACK_RECOVERY, VSS_CF_BACKUP_RECOVERY, VSS_CF_NOT_SYSTEM_STATE, VSS_COMPONENT_FLAGS, VSS_COMPONENT_FLAGS enumeration [VSS], _win32_vss_component_flags, base.vss_component_flags, enumeration [VSS], vswriter/VSS_CF_APP_ROLLBACK_RECOVERY, vswriter/VSS_CF_BACKUP_RECOVERY, vswriter/VSS_CF_NOT_SYSTEM_STATE, vswriter/VSS_COMPONENT_FLAGS
ms.topic: enum
f1_keywords:
- vswriter/VSS_COMPONENT_FLAGS
dev_langs:
 - c++
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
targetos: Windows
req.typenames: VSS_COMPONENT_FLAGS
req.redist: 
ms.custom: 19H1
---

# VSS_COMPONENT_FLAGS enumeration


## -description


The <b>VSS_COMPONENT_FLAGS</b> enumeration is 
    used by writers to indicate support for 
    <a href="https://docs.microsoft.com/windows/desktop/VSS/vssgloss-a">auto-recovery</a>. These 
    values are used in the <b>dwComponentFlags</b> member of 
    the <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/ns-vsbackup-vss_componentinfo">VSS_COMPONENTINFO</a> structure and the 
    <i>dwComponentFlags</i> parameter of 
    the <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addcomponent">IVssCreateWriterMetadata::AddComponent</a> method.


## -enum-fields




### -field VSS_CF_BACKUP_RECOVERY

The writer will need write access to this component after the shadow copy has been created.
      

This flag can be used together with the <b>VSS_VOLSNAP_ATTR_TRANSPORTABLE</b> value of the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> enumeration if the VSS hardware provider supports LUN masking.<b>Windows Vista and Windows Server 2003 with SP1:  </b>This flag is incompatible with <b>VSS_VOLSNAP_ATTR_TRANSPORTABLE</b>.



This flag is not supported for express writers.


### -field VSS_CF_APP_ROLLBACK_RECOVERY

If this is a rollback shadow copy 
      (see the <b>VSS_VOLSNAP_ATTR_ROLLBACK_RECOVERY</b> value of the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> enumeration), the writer for this 
      component will need write access to this component after the shadow copy has been created.
      

This flag can be used together with the <b>VSS_VOLSNAP_ATTR_TRANSPORTABLE</b> value of the <a href="https://docs.microsoft.com/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> enumeration if the VSS hardware provider supports LUN masking.<b>Windows Vista and Windows Server 2003 with SP1:  </b>This flag is incompatible with <b>VSS_VOLSNAP_ATTR_TRANSPORTABLE</b>.



This flag is not supported for express writers.


### -field VSS_CF_NOT_SYSTEM_STATE

This component is not part of system state.

<b>Windows Server 2003 with SP1:  </b>This value is not supported until Windows Vista.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addcomponent">IVssCreateWriterMetadata::AddComponent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vss/ne-vss-vss_backup_schema">VSS_BACKUP_SCHEMA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/ns-vsbackup-vss_componentinfo">VSS_COMPONENTINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/ne-vswriter-vss_usage_type">VSS_USAGE_TYPE</a>
 

 


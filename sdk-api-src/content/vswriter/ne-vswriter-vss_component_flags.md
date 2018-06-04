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

# VSS_COMPONENT_FLAGS enumeration


## -description


The <b>VSS_COMPONENT_FLAGS</b> enumeration is 
    used by writers to indicate support for 
    <a href="vssgloss_a.htm">auto-recovery</a>. These 
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
 

 


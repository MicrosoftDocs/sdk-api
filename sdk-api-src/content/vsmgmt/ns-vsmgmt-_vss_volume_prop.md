---
UID: NS:vsmgmt._VSS_VOLUME_PROP
title: "_VSS_VOLUME_PROP"
author: windows-sdk-content
description: Contains the properties of a shadow copy source volume.
old-location: base\vss_volume_prop.htm
tech.root: VSS
ms.assetid: f17765d5-ccb4-4ede-86e4-36ac80022da0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PVSS_VOLUME_PROP, PVSS_VOLUME_PROP, PVSS_VOLUME_PROP structure pointer [VSS], VSS_VOLUME_PROP, VSS_VOLUME_PROP structure [VSS], _VSS_VOLUME_PROP, base.vss_volume_prop, vsmgmt/PVSS_VOLUME_PROP, vsmgmt/VSS_VOLUME_PROP"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - VsMgmt.h
api_name:
 - VSS_VOLUME_PROP
product: Windows
targetos: Windows
req.typenames: VSS_VOLUME_PROP, *PVSS_VOLUME_PROP
req.redist: 
---

# _VSS_VOLUME_PROP structure


## -description


The <b>VSS_VOLUME_PROP</b> structure contains the 
    properties of a shadow copy source volume.


## -struct-fields




### -field m_pwszVolumeName

The volume name, in \\?\<i>Volume</i>{<i>GUID</i>}\ format.


### -field m_pwszVolumeDisplayName

A pointer to a null-terminated Unicode string that contains the shortest mount 
      point that can be displayed to the user. The mount point can be a drive letter, for example, C:\, or a mounted folder, for example, C:\WriterData\Archive.


## -see-also




<a href="https://msdn.microsoft.com/4d787229-671a-422c-a935-39ae11073a5e">VSS_MGMT_OBJECT_UNION</a>



<a href="https://msdn.microsoft.com/20cf12e4-4611-4e39-9f6f-e29f15e58b36">Volume Shadow Copy API Structures</a>
 

 


---
UID: NS:vsmgmt._VSS_DIFF_VOLUME_PROP
title: "_VSS_DIFF_VOLUME_PROP"
author: windows-driver-content
description: Describes a shadow copy storage area volume.
old-location: base\vss_diff_volume_prop.htm
old-project: VSS
ms.assetid: c4a20583-7fee-4ae1-97ed-d80b2a7539e3
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: "*PVSS_DIFF_VOLUME_PROP, PVSS_DIFF_VOLUME_PROP, PVSS_DIFF_VOLUME_PROP structure pointer [VSS], VSS_DIFF_VOLUME_PROP, VSS_DIFF_VOLUME_PROP structure [VSS], _VSS_DIFF_VOLUME_PROP, base.vss_diff_volume_prop, vsmgmt/PVSS_DIFF_VOLUME_PROP, vsmgmt/VSS_DIFF_VOLUME_PROP"
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
req.typenames: VSS_DIFF_VOLUME_PROP, *PVSS_DIFF_VOLUME_PROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	VsMgmt.h
api_name:
-	VSS_DIFF_VOLUME_PROP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VSS_DIFF_VOLUME_PROP structure


## -description


The <b>VSS_DIFF_VOLUME_PROP</b> structure 
   describes a shadow copy storage area volume.


## -struct-fields




### -field m_pwszVolumeName

The shadow copy storage area volume name, in <b>\\?\</b><i>Volume</i><b>{</b><i>GUID</i><b>}\</b> format.


### -field m_pwszVolumeDisplayName

Points to a null-terminated Unicode string that can be displayed to a user, for example 
      <i>C</i><b>:\</b>, for the shadow copy storage area volume.


### -field m_llVolumeFreeSpace

Free space, in bytes, on the shadow copy storage area volume.


### -field m_llVolumeTotalSpace

Total space, in bytes, on the shadow copy storage area volume.


## -see-also




<a href="https://msdn.microsoft.com/4d787229-671a-422c-a935-39ae11073a5e">VSS_MGMT_OBJECT_UNION</a>
 

 


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
 

 


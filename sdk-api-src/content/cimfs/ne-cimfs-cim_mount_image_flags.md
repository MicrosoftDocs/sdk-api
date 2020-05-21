---
UID: NE:cimfs.CIM_MOUNT_IMAGE_FLAGS
title: CIM_MOUNT_IMAGE_FLAGS
ms.date: 9/9/2019
ms.keywords: CIM_MOUNT_IMAGE_FLAGS
ms.topic: language-reference
targetos: Windows
product: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: cimfs.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - cimfs.h
api_name:
 - CIM_MOUNT_IMAGE_FLAGS
---

## -description
Flags that can be used to modify the behavior of CimMountImage.

## -enum-fields

### -field CIM_MOUNT_IMAGE_NONE
When no flags are specified the mounted image will contain the entire contents of the image.

### -field CIM_MOUNT_CHILD_ONLY
Specifies that the mounted image should contain only the contents of the leaf node child of a forked image. The parent image contents are masked in the mounted image.

## -remarks

## -see-also


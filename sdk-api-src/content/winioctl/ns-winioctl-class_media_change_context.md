---
UID: NS:winioctl._CLASS_MEDIA_CHANGE_CONTEXT
title: CLASS_MEDIA_CHANGE_CONTEXT
description: Contains information associated with a media change event.
helpviewer_keywords: ["*PCLASS_MEDIA_CHANGE_CONTEXT","CLASS_MEDIA_CHANGE_CONTEXT","CLASS_MEDIA_CHANGE_CONTEXT structure","MediaNotPresent","MediaPresent","MediaUnavailable","MediaUnknown","PCLASS_MEDIA_CHANGE_CONTEXT","PCLASS_MEDIA_CHANGE_CONTEXT structure pointer","_win32_class_media_change_context_str","base.class_media_change_context_str","winioctl/CLASS_MEDIA_CHANGE_CONTEXT","winioctl/PCLASS_MEDIA_CHANGE_CONTEXT"]
old-location: base\class_media_change_context_str.htm
tech.root: base
ms.assetid: c89da554-3dc5-4278-8afe-8da9cc0a0120
ms.date: 12/05/2018
ms.keywords: '*PCLASS_MEDIA_CHANGE_CONTEXT, CLASS_MEDIA_CHANGE_CONTEXT, CLASS_MEDIA_CHANGE_CONTEXT structure, MediaNotPresent, MediaPresent, MediaUnavailable, MediaUnknown, PCLASS_MEDIA_CHANGE_CONTEXT, PCLASS_MEDIA_CHANGE_CONTEXT structure pointer, _win32_class_media_change_context_str, base.class_media_change_context_str, winioctl/CLASS_MEDIA_CHANGE_CONTEXT, winioctl/PCLASS_MEDIA_CHANGE_CONTEXT'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
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
req.typenames: CLASS_MEDIA_CHANGE_CONTEXT, *PCLASS_MEDIA_CHANGE_CONTEXT
req.redist: 
f1_keywords:
 - _CLASS_MEDIA_CHANGE_CONTEXT
 - winioctl/_CLASS_MEDIA_CHANGE_CONTEXT
 - PCLASS_MEDIA_CHANGE_CONTEXT
 - winioctl/PCLASS_MEDIA_CHANGE_CONTEXT
 - CLASS_MEDIA_CHANGE_CONTEXT
 - winioctl/CLASS_MEDIA_CHANGE_CONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - CLASS_MEDIA_CHANGE_CONTEXT
---

# CLASS_MEDIA_CHANGE_CONTEXT structure


## -description

Contains information associated with a media change event.

## -struct-fields

### -field MediaChangeCount

The number of times that media has been changed since system startup.

### -field NewState

The state information. This member can be one of the following values from the 
      <b>MEDIA_CHANGE_DETECTION_STATE</b> enumeration type.



#### MediaUnknown (0)



#### MediaPresent (1)



#### MediaNotPresent (2)



#### MediaUnavailable (3)

## -see-also

<a href="/windows/desktop/DevIO/dbt-customevent">DBT_CUSTOMEVENT</a>



<a href="/windows/desktop/DevIO/dbt-deviceremovecomplete">DBT_DEVICEREMOVECOMPLETE</a>
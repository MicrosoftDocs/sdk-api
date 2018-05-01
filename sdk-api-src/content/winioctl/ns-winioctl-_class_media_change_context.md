---
UID: NS:winioctl._CLASS_MEDIA_CHANGE_CONTEXT
title: "_CLASS_MEDIA_CHANGE_CONTEXT"
author: windows-driver-content
description: Contains information associated with a media change event.
old-location: base\class_media_change_context_str.htm
old-project: DevIO
ms.assetid: c89da554-3dc5-4278-8afe-8da9cc0a0120
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: "*PCLASS_MEDIA_CHANGE_CONTEXT, CLASS_MEDIA_CHANGE_CONTEXT, CLASS_MEDIA_CHANGE_CONTEXT structure, MediaNotPresent, MediaPresent, MediaUnavailable, MediaUnknown, PCLASS_MEDIA_CHANGE_CONTEXT, PCLASS_MEDIA_CHANGE_CONTEXT structure pointer, _CLASS_MEDIA_CHANGE_CONTEXT, _win32_class_media_change_context_str, base.class_media_change_context_str, winioctl/CLASS_MEDIA_CHANGE_CONTEXT, winioctl/PCLASS_MEDIA_CHANGE_CONTEXT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: CLASS_MEDIA_CHANGE_CONTEXT, *PCLASS_MEDIA_CHANGE_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	CLASS_MEDIA_CHANGE_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CLASS_MEDIA_CHANGE_CONTEXT structure


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




<a href="https://msdn.microsoft.com/6e66fa93-0cd7-4202-83eb-cddc668525ae">DBT_CUSTOMEVENT</a>



<a href="https://msdn.microsoft.com/e25d35b9-f8f1-4850-996c-e1cb393cca66">DBT_DEVICEREMOVECOMPLETE</a>
 

 


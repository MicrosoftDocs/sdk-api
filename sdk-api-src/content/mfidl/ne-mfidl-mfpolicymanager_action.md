---
UID: NE:mfidl._MFPOLICYMANAGER_ACTION
title: MFPOLICYMANAGER_ACTION (mfidl.h)
description: Defines actions that can be performed on a stream.
helpviewer_keywords: ["74cee983-e084-458b-b615-5447cca9abbc","MFPOLICYMANAGER_ACTION","MFPOLICYMANAGER_ACTION enumeration [Media Foundation]","PEACTION_COPY","PEACTION_EXPORT","PEACTION_EXTRACT","PEACTION_LAST","PEACTION_NO","PEACTION_PLAY","PEACTION_RESERVED1","PEACTION_RESERVED2","PEACTION_RESERVED3","mf.mfpolicymanager_action","mfidl/MFPOLICYMANAGER_ACTION","mfidl/PEACTION_COPY","mfidl/PEACTION_EXPORT","mfidl/PEACTION_EXTRACT","mfidl/PEACTION_LAST","mfidl/PEACTION_NO","mfidl/PEACTION_PLAY","mfidl/PEACTION_RESERVED1","mfidl/PEACTION_RESERVED2","mfidl/PEACTION_RESERVED3"]
old-location: mf\mfpolicymanager_action.htm
tech.root: mf
ms.assetid: 74cee983-e084-458b-b615-5447cca9abbc
ms.date: 12/05/2018
ms.keywords: 74cee983-e084-458b-b615-5447cca9abbc, MFPOLICYMANAGER_ACTION, MFPOLICYMANAGER_ACTION enumeration [Media Foundation], PEACTION_COPY, PEACTION_EXPORT, PEACTION_EXTRACT, PEACTION_LAST, PEACTION_NO, PEACTION_PLAY, PEACTION_RESERVED1, PEACTION_RESERVED2, PEACTION_RESERVED3, mf.mfpolicymanager_action, mfidl/MFPOLICYMANAGER_ACTION, mfidl/PEACTION_COPY, mfidl/PEACTION_EXPORT, mfidl/PEACTION_EXTRACT, mfidl/PEACTION_LAST, mfidl/PEACTION_NO, mfidl/PEACTION_PLAY, mfidl/PEACTION_RESERVED1, mfidl/PEACTION_RESERVED2, mfidl/PEACTION_RESERVED3
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MFPOLICYMANAGER_ACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFPOLICYMANAGER_ACTION
 - mfidl/_MFPOLICYMANAGER_ACTION
 - MFPOLICYMANAGER_ACTION
 - mfidl/MFPOLICYMANAGER_ACTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFPOLICYMANAGER_ACTION
---

# MFPOLICYMANAGER_ACTION enumeration


## -description

Defines actions that can be performed on a stream.

## -enum-fields

### -field PEACTION_NO:0

No action.

### -field PEACTION_PLAY:1

Play the stream.

### -field PEACTION_COPY:2

Copy the stream.

### -field PEACTION_EXPORT:3

Export the stream to another format.

### -field PEACTION_EXTRACT:4

Extract the data from the stream and pass it to the application. For example, acoustic echo cancellation requires this action.

### -field PEACTION_RESERVED1:5

Reserved.

### -field PEACTION_RESERVED2:6

Reserved.

### -field PEACTION_RESERVED3:7

Reserved.

### -field PEACTION_LAST:7

Last member of the enumeration.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>

---
UID: NE:mbnapi.MBN_VOICE_CLASS
title: MBN_VOICE_CLASS
author: windows-sdk-content
description: The MBN_VOICE_CLASS enumerated type specifies a device's voice capabilities and how they interact with the data service.
old-location: mbn\mbn_voice_class.htm
tech.root: mbn
ms.assetid: d2654e97-4020-449f-9622-39392309d6f3
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: MBN_VOICE_CLASS, MBN_VOICE_CLASS enumeration [Microsoft Broadband Networks], MBN_VOICE_CLASS_NONE, MBN_VOICE_CLASS_NO_VOICE, MBN_VOICE_CLASS_SEPARATE_VOICE_DATA, MBN_VOICE_CLASS_SIMULTANEOUS_VOICE_DATA, mbn.mbn_voice_class, mbnapi/MBN_VOICE_CLASS, mbnapi/MBN_VOICE_CLASS_NONE, mbnapi/MBN_VOICE_CLASS_NO_VOICE, mbnapi/MBN_VOICE_CLASS_SEPARATE_VOICE_DATA, mbnapi/MBN_VOICE_CLASS_SIMULTANEOUS_VOICE_DATA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - mbnapi.h
api_name:
 - MBN_VOICE_CLASS
product: Windows
targetos: Windows
req.typenames: MBN_VOICE_CLASS
req.redist: 
---

# MBN_VOICE_CLASS enumeration


## -description


 The <b>MBN_VOICE_CLASS</b> enumerated type specifies a device's voice capabilities and how they interact with the data service.


## -enum-fields




### -field MBN_VOICE_CLASS_NONE

The device voice class is unknown.


### -field MBN_VOICE_CLASS_NO_VOICE

The device does not support voice calls.


### -field MBN_VOICE_CLASS_SEPARATE_VOICE_DATA

The device supports voice calls, but does not support simultaneous voice and data.


### -field MBN_VOICE_CLASS_SIMULTANEOUS_VOICE_DATA

The device supports simultaneous voice and data.


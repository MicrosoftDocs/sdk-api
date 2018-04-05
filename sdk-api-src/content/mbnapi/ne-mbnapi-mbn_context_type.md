---
UID: NE:mbnapi.MBN_CONTEXT_TYPE
title: MBN_CONTEXT_TYPE
author: windows-driver-content
description: The MBN_CONTEXT_TYPE enumerated type specifies the represented context type.
old-location: mbn\mbn_context_type.htm
old-project: mbn
ms.assetid: 40ab2190-9fc2-43e2-9a8a-29fcaa5b035f
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: MBN_CONTEXT_TYPE, MBN_CONTEXT_TYPE enumeration [Microsoft Broadband Networks], MBN_CONTEXT_TYPE_CUSTOM, MBN_CONTEXT_TYPE_INTERNET, MBN_CONTEXT_TYPE_NONE, MBN_CONTEXT_TYPE_PURCHASE, MBN_CONTEXT_TYPE_VIDEO_SHARE, MBN_CONTEXT_TYPE_VOICE, MBN_CONTEXT_TYPE_VPN, mbn.mbn_context_type, mbnapi/MBN_CONTEXT_TYPE, mbnapi/MBN_CONTEXT_TYPE_CUSTOM, mbnapi/MBN_CONTEXT_TYPE_INTERNET, mbnapi/MBN_CONTEXT_TYPE_NONE, mbnapi/MBN_CONTEXT_TYPE_PURCHASE, mbnapi/MBN_CONTEXT_TYPE_VIDEO_SHARE, mbnapi/MBN_CONTEXT_TYPE_VOICE, mbnapi/MBN_CONTEXT_TYPE_VPN
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MBN_CONTEXT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mbnapi.h
api_name:
-	MBN_CONTEXT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: Mapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# MBN_CONTEXT_TYPE enumeration


## -description


The <b>MBN_CONTEXT_TYPE</b> enumerated type specifies the represented context type.


## -enum-fields




### -field MBN_CONTEXT_TYPE_NONE

Context has not yet provisioned for this ID.


### -field MBN_CONTEXT_TYPE_INTERNET

Context represents a connection to the internet.


### -field MBN_CONTEXT_TYPE_VPN

Context represents a connection to a VPN or corporate network.


### -field MBN_CONTEXT_TYPE_VOICE

Context represents a connection to VoIP service.


### -field MBN_CONTEXT_TYPE_VIDEO_SHARE

Context represents a connection to a video share service.


### -field MBN_CONTEXT_TYPE_CUSTOM

Context represents a connection to a custom service.


### -field MBN_CONTEXT_TYPE_PURCHASE

Windows 8 or later: Context represents a purchase connection such as a walled garden, hot-lining, or captive portal.


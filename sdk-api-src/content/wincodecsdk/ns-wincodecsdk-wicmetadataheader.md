---
UID: NS:wincodecsdk.WICMetadataHeader
title: WICMetadataHeader
author: windows-driver-content
description: Represents metadata header.
old-location: wic\_wic_codec_wicmetadataheader.htm
old-project: wic
ms.assetid: f643b163-55b2-4691-a4eb-fc162949e936
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: WICMetadataHeader, WICMetadataHeader structure [Windows Imaging Component], _wic_codec_wicmetadataheader, wic._wic_codec_wicmetadataheader, wincodecsdk/WICMetadataHeader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICMetadataHeader
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincodecsdk.h
api_name:
-	WICMetadataHeader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WICMetadataHeader structure


## -description


Represents metadata header.


## -struct-fields




### -field Position

Type: <b>ULARGE_INTEGER</b>

The position of the header.


### -field Length

Type: <b>ULONG</b>

The length of the header.


### -field Header

Type: <b>BYTE*</b>

Pointer to the header.


### -field DataOffset

Type: <b>ULARGE_INTEGER</b>

The offset of the header.


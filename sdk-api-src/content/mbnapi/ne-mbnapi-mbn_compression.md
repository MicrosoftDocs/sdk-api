---
UID: NE:mbnapi.MBN_COMPRESSION
title: MBN_COMPRESSION
author: windows-sdk-content
description: The MBN_COMPRESSION enumerated type specifies whether compression is to be used in the data link for header and data.
old-location: mbn\mbn_compression.htm
old-project: mbn
ms.assetid: fd5cbfba-2eea-4d81-9733-33feb402fd8d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: MBN_COMPRESSION, MBN_COMPRESSION enumeration [Microsoft Broadband Networks], MBN_COMPRESSION_ENABLE, MBN_COMPRESSION_NONE, mbn.mbn_compression, mbnapi/MBN_COMPRESSION, mbnapi/MBN_COMPRESSION_ENABLE, mbnapi/MBN_COMPRESSION_NONE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mbnapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
tech.root: 
req.typenames: MBN_COMPRESSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_COMPRESSION
product: Windows
targetos: Windows
req.lib: 
req.dll: Mapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# MBN_COMPRESSION enumeration


## -description


The <b>MBN_COMPRESSION</b> enumerated type specifies whether compression is to be used in the data link for header and data.

This type is applicable only for GSM devices.


## -enum-fields




### -field MBN_COMPRESSION_NONE

Data headers are not compressed.


### -field MBN_COMPRESSION_ENABLE

Data headers are compressed.


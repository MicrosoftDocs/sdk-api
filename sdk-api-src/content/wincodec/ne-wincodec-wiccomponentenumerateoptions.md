---
UID: NE:wincodec.WICComponentEnumerateOptions
title: WICComponentEnumerateOptions
author: windows-sdk-content
description: Specifies component enumeration options.
old-location: wic\_wic_codec_wiccomponentenumerateoptions.htm
old-project: wic
ms.assetid: 52cc0860-6164-4400-8e81-03eb0c44904e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WICComponentEnumerateBuiltInOnly, WICComponentEnumerateDefault, WICComponentEnumerateDisabled, WICComponentEnumerateOptions, WICComponentEnumerateOptions enumeration [Windows Imaging Component], WICComponentEnumerateRefresh, WICComponentEnumerateUnsigned, _wic_codec_wiccomponentenumerateoptions, wic._wic_codec_wiccomponentenumerateoptions, wincodec/WICComponentEnumerateBuiltInOnly, wincodec/WICComponentEnumerateDefault, wincodec/WICComponentEnumerateDisabled, wincodec/WICComponentEnumerateOptions, wincodec/WICComponentEnumerateRefresh, wincodec/WICComponentEnumerateUnsigned
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wincodec.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WICComponentEnumerateOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICComponentEnumerateOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WICComponentEnumerateOptions enumeration


## -description


Specifies component enumeration options.


## -enum-fields




### -field WICComponentEnumerateDefault

Enumerate any components that are not disabled. Because this value is 0x0, it is always included with the other options.


### -field WICComponentEnumerateRefresh

Force a read of the registry before enumerating components.


### -field WICComponentEnumerateDisabled

Include disabled components in the enumeration. The set of disabled components is disjoint with the set of default enumerated components


### -field WICComponentEnumerateUnsigned

Include unsigned components in the enumeration. This option has no effect.


### -field WICComponentEnumerateBuiltInOnly

At the end of component enumeration, filter out any components that are not Windows provided.


### -field WICCOMPONENTENUMERATEOPTIONS_FORCE_DWORD




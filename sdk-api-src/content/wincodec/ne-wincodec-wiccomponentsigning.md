---
UID: NE:wincodec.WICComponentSigning
title: WICComponentSigning
author: windows-sdk-content
description: Specifies the component signing status.
old-location: wic\_wic_codec_wiccomponentsigning.htm
old-project: wic
ms.assetid: 64f3de6d-15da-4cc8-ad74-57759bcd4d07
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WICComponentDisabled, WICComponentSafe, WICComponentSigned, WICComponentSigning, WICComponentSigning enumeration [Windows Imaging Component], WICComponentUnsigned, _wic_codec_wiccomponentsigning, wic._wic_codec_wiccomponentsigning, wincodec/WICComponentDisabled, wincodec/WICComponentSafe, wincodec/WICComponentSigned, wincodec/WICComponentSigning, wincodec/WICComponentUnsigned
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wincodec.h
req.include-header: 
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
req.typenames: WICComponentSigning
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICComponentSigning
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WICComponentSigning enumeration


## -description


Specifies the component signing status.


## -enum-fields




### -field WICComponentSigned

A signed component.


### -field WICComponentUnsigned

An unsigned component


### -field WICComponentSafe

A component is safe.
            

Components that do not have a binary component to sign, such as a pixel format, should return this value.


### -field WICComponentDisabled

A component has been disabled.


### -field WICCOMPONENTSIGNING_FORCE_DWORD




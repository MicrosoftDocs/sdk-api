---
UID: NE:d2d1.D2D1_PRESENT_OPTIONS
title: D2D1_PRESENT_OPTIONS
author: windows-sdk-content
description: Describes how a render target behaves when it presents its content. This enumeration allows a bitwise combination of its member values.
old-location: direct2d\D2D1_PRESENT_OPTIONS.htm
tech.root: direct2d
ms.assetid: 56178ee9-7d35-42e1-97f8-62835010f277
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: D2D1_PRESENT_OPTIONS, D2D1_PRESENT_OPTIONS enumeration [Direct2D], D2D1_PRESENT_OPTIONS_IMMEDIATELY, D2D1_PRESENT_OPTIONS_NONE, D2D1_PRESENT_OPTIONS_RETAIN_CONTENTS, d2d1/D2D1_PRESENT_OPTIONS, d2d1/D2D1_PRESENT_OPTIONS_IMMEDIATELY, d2d1/D2D1_PRESENT_OPTIONS_NONE, d2d1/D2D1_PRESENT_OPTIONS_RETAIN_CONTENTS, direct2d.D2D1_PRESENT_OPTIONS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_PRESENT_OPTIONS
product: Windows
targetos: Windows
req.typenames: D2D1_PRESENT_OPTIONS
req.redist: 
---

# D2D1_PRESENT_OPTIONS enumeration


## -description


Describes how a render target behaves when it presents its content. This enumeration allows a bitwise combination of its member values.


## -enum-fields




### -field D2D1_PRESENT_OPTIONS_NONE

The render target waits until the display refreshes to present and discards the frame upon presenting.


### -field D2D1_PRESENT_OPTIONS_RETAIN_CONTENTS

The render target does not discard the frame upon presenting.


### -field D2D1_PRESENT_OPTIONS_IMMEDIATELY

The render target does not wait until the display refreshes to present.


### -field D2D1_PRESENT_OPTIONS_FORCE_DWORD




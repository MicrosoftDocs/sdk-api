---
UID: NN:shobjidl_core.IShellLinkA
title: IShellLinkA (shobjidl_core.h)
description: Exposes methods that create, modify, and resolve Shell links. (ANSI)
helpviewer_keywords: ["IShellLink","IShellLink interface [Windows Shell]","IShellLink interface [Windows Shell]","described","IShellLinkA","IShellLinkW","_win32_IShellLink","_win32_IShellLink_cpp","shell.IShellLink","shobjidl_core/IShellLink"]
old-location: shell\IShellLink.htm
tech.root: shell
ms.assetid: 67982d28-27ce-4482-b588-10fec8143750
ms.date: 12/05/2018
ms.keywords: IShellLink, IShellLink interface [Windows Shell], IShellLink interface [Windows Shell],described, IShellLinkA, IShellLinkW, _win32_IShellLink, _win32_IShellLink_cpp, shell.IShellLink, shobjidl_core/IShellLink
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellLinkA
 - shobjidl_core/IShellLinkA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellLink
 - IShellLinkW
 - IShellLinkA
---

# IShellLinkA interface


## -description

Exposes methods that create, modify, and resolve Shell links.

## -inheritance

The <b>IShellLink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellLink</b> also has these types of members:

## -remarks

<div class="alert"><b>Note</b>  This interface cannot be used to create a link to a URL.</div>
<div> </div>
The <b>IShellLink</b> interface has an ANSI version (<b>IShellLinkA</b>) and a Unicode version (<b>IShellLinkW</b>). The version that will be used depends on whether you compile for ANSI or Unicode.




> [!NOTE]
> The shobjidl_core.h header defines IShellLink as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

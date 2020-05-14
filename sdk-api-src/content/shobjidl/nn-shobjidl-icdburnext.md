---
UID: NN:shobjidl.ICDBurnExt
title: ICDBurnExt (shobjidl.h)
description: ICDBurnExt may be altered or unavailable.helpviewer_keywords: ["ICDBurnExt","ICDBurnExt interface [Windows Shell]","ICDBurnExt interface [Windows Shell]","described","_shell_ICDBurnExt","shell.ICDBurnExt","shobjidl/ICDBurnExt"]
old-location: shell\ICDBurnExt.htm
tech.root: shell
ms.assetid: e87a635b-9614-49e1-8633-f7cbb5050b9a
ms.date: 12/05/2018
ms.keywords: ICDBurnExt, ICDBurnExt interface [Windows Shell], ICDBurnExt interface [Windows Shell],described, _shell_ICDBurnExt, shell.ICDBurnExt, shobjidl/ICDBurnExt
f1_keywords:
- shobjidl/ICDBurnExt
dev_langs:
- c++
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shobjidl.h
api_name:
- ICDBurnExt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICDBurnExt interface


## -description


<p class="CCE_Message">[<b>ICDBurnExt</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Exposes a single method that determines content types supported by a CD writing extension.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICDBurnExt</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICDBurnExt</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICDBurnExt</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-icdburnext-getsupportedactiontypes">GetSupportedActionTypes</a>
</td>
<td align="left" width="63%">
Determines the supported data type for a CD writing extension.

</td>
</tr>
</table> 


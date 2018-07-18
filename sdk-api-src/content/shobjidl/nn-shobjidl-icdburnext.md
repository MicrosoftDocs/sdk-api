---
UID: NN:shobjidl.ICDBurnExt
title: ICDBurnExt
author: windows-sdk-content
description: ICDBurnExt may be altered or unavailable.
old-location: shell\ICDBurnExt.htm
old-project: shell
ms.assetid: e87a635b-9614-49e1-8633-f7cbb5050b9a
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ICDBurnExt, ICDBurnExt interface [Windows Shell], ICDBurnExt interface [Windows Shell],described, _shell_ICDBurnExt, shell.ICDBurnExt, shobjidl/ICDBurnExt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - ICDBurnExt
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# ICDBurnExt interface


## -description


<p class="CCE_Message">[<b>ICDBurnExt</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Exposes a single method that determines content types supported by a CD writing extension.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICDBurnExt</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICDBurnExt</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/46d0fe58-b8aa-42a8-811e-9762185bb8cc">GetSupportedActionTypes</a>
</td>
<td align="left" width="63%">
Determines the supported data type for a CD writing extension.

</td>
</tr>
</table> 


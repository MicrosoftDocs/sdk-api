---
UID: NN:shobjidl.IStreamUnbufferedInfo
title: IStreamUnbufferedInfo
author: windows-sdk-content
description: Exposes a method that determines the sector size as an aid to byte alignment.
old-location: shell\IStreamUnbufferedInfo.htm
old-project: shell
ms.assetid: 51c28816-91a2-47cf-86b9-327a538ebca1
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IStreamUnbufferedInfo, IStreamUnbufferedInfo interface [Windows Shell], IStreamUnbufferedInfo interface [Windows Shell],described, _shell_IStreamUnbufferedInfo, shell.IStreamUnbufferedInfo, shobjidl/IStreamUnbufferedInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IStreamUnbufferedInfo
product: Windows
targetos: Windows
req.lib: Comdlg32.lib
req.dll: Shell32.dll (version 6.0.6000 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# IStreamUnbufferedInfo interface


## -description


Exposes a method that determines the sector size as an aid to byte alignment.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamUnbufferedInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStreamUnbufferedInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamUnbufferedInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2194de8b-25bd-4eeb-8a67-d5bd22947497">GetSectorSize</a>
</td>
<td align="left" width="63%">
Retrieves the number of bytes per sector on the disk currently being used.  When using unbuffered I/O, it is important to know the size of the sectors on the disk being read in order to ensure proper byte alignment.

</td>
</tr>
</table> 


---
UID: NN:shimgdata.IShellImageDataAbort
title: IShellImageDataAbort (shimgdata.h)
author: windows-sdk-content
description: Exposes a single method used to abort IShellImageData processes.
old-location: shell\IShellImageDataAbort.htm
tech.root: shell
ms.assetid: 98a79c41-a384-4486-af51-a33cd5f0750e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShellImageDataAbort, IShellImageDataAbort interface [Windows Shell], IShellImageDataAbort interface [Windows Shell],described, _shell_IShellImageDataAbort, shell.IShellImageDataAbort, shimgdata/IShellImageDataAbort
ms.topic: interface
f1_keywords: 
 - "shimgdata/IShellImageDataAbort"
req.header: shimgdata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shimgdata.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageDataAbort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellImageDataAbort interface


## -description


Exposes a single method used to abort <a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> processes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellImageDataAbort</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellImageDataAbort</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellImageDataAbort</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedataabort-queryabort">QueryAbort</a>
</td>
<td align="left" width="63%">
Aborts an <a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> process such as <a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-decode">Decode</a>, <a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-draw">Draw</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-scale">Scale</a>. This is a callback method.

</td>
</tr>
</table> 


## -remarks



This interface is not expected to be available in later versions of Windows. It is recommended that Windows GDI+ APIs be used in place of <a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> methods.

This interface was not included in a public header file prior to Windows Vista.




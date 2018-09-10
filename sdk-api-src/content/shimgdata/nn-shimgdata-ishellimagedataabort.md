---
UID: NN:shimgdata.IShellImageDataAbort
title: IShellImageDataAbort
author: windows-sdk-content
description: Exposes a single method used to abort IShellImageData processes.
old-location: shell\IShellImageDataAbort.htm
tech.root: shell
ms.assetid: 98a79c41-a384-4486-af51-a33cd5f0750e
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IShellImageDataAbort, IShellImageDataAbort interface [Windows Shell], IShellImageDataAbort interface [Windows Shell],described, _shell_IShellImageDataAbort, shell.IShellImageDataAbort, shimgdata/IShellImageDataAbort
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# IShellImageDataAbort interface


## -description


Exposes a single method used to abort <a href="https://msdn.microsoft.com/935e651c-4dcd-4317-847e-34adf656035c">IShellImageData</a> processes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellImageDataAbort</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellImageDataAbort</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/88823fe3-efde-4ee1-9b4f-685f8df03b29">QueryAbort</a>
</td>
<td align="left" width="63%">
Aborts an <a href="https://msdn.microsoft.com/935e651c-4dcd-4317-847e-34adf656035c">IShellImageData</a> process such as <a href="https://msdn.microsoft.com/954424d6-cb90-46c1-a850-4e1113dfe2e4">Decode</a>, <a href="https://msdn.microsoft.com/35989c3b-15b9-4503-a883-99df730b2a80">Draw</a>, or <a href="https://msdn.microsoft.com/ebcc9cc1-b6ee-4fb9-9125-54d6a9ee9434">Scale</a>. This is a callback method.

</td>
</tr>
</table> 


## -remarks



This interface is not expected to be available in later versions of Windows. It is recommended that Windows GDI+ APIs be used in place of <a href="https://msdn.microsoft.com/935e651c-4dcd-4317-847e-34adf656035c">IShellImageData</a> methods.

This interface was not included in a public header file prior to Windows Vista.




---
UID: NN:shlobj.IShellFolderBand
title: IShellFolderBand (shlobj.h)
author: windows-sdk-content
description: IShellFolderBand may be altered or unavailable.
old-location: shell\IShellFolderBand.htm
tech.root: shell
ms.assetid: 88ae35ea-6ff9-431c-848b-84fc61d3c690
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShellFolderBand, IShellFolderBand interface [Windows Shell], IShellFolderBand interface [Windows Shell],described, _win32_IShellFolderBand, shell.IShellFolderBand, shlobj/IShellFolderBand
ms.topic: interface
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellFolderBand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderBand interface


## -description


<p class="CCE_Message">[<b>IShellFolderBand</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Exposes methods that manage folder bands. The Quick Launch bar is an example of a folder band.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellFolderBand</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellFolderBand</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellFolderBand</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a42ba12-987a-4b43-9d95-085a5e896245">GetBandInfoSFB</a>
</td>
<td align="left" width="63%">
Gets information concerning an <b>IShellFolderBand</b> object and places it in a <a href="https://msdn.microsoft.com/7067f563-383d-469f-abcf-3e1ea28dc956">BANDINFOSFB</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f0582d2-b079-4b97-8da0-211b6ef1b8f3">InitializeSFB</a>
</td>
<td align="left" width="63%">
Initializes an <b>IShellFolderBand</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b1a219f-60a3-4073-8293-2e9e1c6459d9">SetBandInfoSFB</a>
</td>
<td align="left" width="63%">
Uses the information in a <a href="https://msdn.microsoft.com/7067f563-383d-469f-abcf-3e1ea28dc956">BANDINFOSFB</a> structure to set the band information for a <b>IShellFolderBand</b> object.

</td>
</tr>
</table> 


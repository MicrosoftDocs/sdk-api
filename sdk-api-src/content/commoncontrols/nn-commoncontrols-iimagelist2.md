---
UID: NN:commoncontrols.IImageList2
title: IImageList2
author: windows-sdk-content
description: Extends IImageList by providing additional methods for manipulating and interacting with image lists.
old-location: controls\IImageList2.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\iimagelist2.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: IImageList2, IImageList2 interface [Windows Controls], IImageList2 interface [Windows Controls],described, _shell_IImageList2, _shell_IImageList2_cpp, commoncontrols/IImageList2, controls.IImageList2, controls._shell_IImageList2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Commoncontrols.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OFNOTIFYW, *LPOFNOTIFYW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Commoncontrols.h
api_name:
-	IImageList2
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
---

# IImageList2 interface


## -description


Extends <a href="https://msdn.microsoft.com/02e397a4-22fa-49fb-8103-376aa5ebc77a">IImageList</a> by providing additional methods for manipulating and interacting with image lists.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IImageList2</b> interface inherits from <a href="https://msdn.microsoft.com/02e397a4-22fa-49fb-8103-376aa5ebc77a">IImageList</a>. <b>IImageList2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IImageList2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0F190B9F-23FF-40CE-8344-B498B99F3327">DiscardImages</a>
</td>
<td align="left" width="63%">
Discards images from list, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D202F7B5-A240-4791-8EDA-15BEA8170140">ForceImagePresent</a>
</td>
<td align="left" width="63%">
Forces an image present, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/706EC249-5F28-4DB0-B201-B6BC4826C5BD">GetCallback</a>
</td>
<td align="left" width="63%">
Gets an image list callback object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CB688326-CCB1-4F7E-B3AF-CFF0A553AA64">GetOriginalSize</a>
</td>
<td align="left" width="63%">
Gets the original size of a specified image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D6402FCB-8E84-4F46-9B88-C0AFCEA66A9A">GetStatistics</a>
</td>
<td align="left" width="63%">
Gets an image list statistics structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an image list, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BFCE0745-5579-4713-8BE5-71E532E3B84E">PreloadImages</a>
</td>
<td align="left" width="63%">
Preloads images, as specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/719C6188-8B2C-4C51-8F87-B927A04353F1">Replace2</a>
</td>
<td align="left" width="63%">
Replaces an image in an image list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C18AA1DC-1834-45CE-8EE1-DF3C930BB41F">ReplaceFromImageList</a>
</td>
<td align="left" width="63%">
Replaces an image in one image list with an image from another image list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1701C1BE-84E2-43EB-9A82-58B684D1057D">Resize</a>
</td>
<td align="left" width="63%">
Resizes the current image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0A837A70-FE57-4BC1-8688-E1465A3BF63D">SetCallback</a>
</td>
<td align="left" width="63%">
Sets an image list callback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F9C67C91-0A28-47B8-82C0-DEC2E46FA19B">SetOriginalSize</a>
</td>
<td align="left" width="63%">
Sets the original size of a specified image.

</td>
</tr>
</table> 


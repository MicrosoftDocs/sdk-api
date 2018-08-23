---
UID: NN:strmif.IDvdCmd
title: IDvdCmd
author: windows-sdk-content
description: The IDvdCmd interface waits for DVD commands to start or end.The DVD Navigator creates synchronization objects that expose this interface.
old-location: dshow\idvdcmd.htm
old-project: DirectShow
ms.assetid: 85f9b208-ddc2-4d9c-a30b-b666c81a49d2
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IDvdCmd, IDvdCmd interface [DirectShow], IDvdCmd interface [DirectShow],described, IDvdCmdInterface, dshow.idvdcmd, strmif/IDvdCmd
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdCmd
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdCmd interface


## -description



The <code>IDvdCmd</code> interface waits for DVD commands to start or end.

The DVD Navigator creates synchronization objects that expose this interface. The application can use the object to block the DVD Navigator until the command starts or completes. For more information on using this interface, see <a href="https://msdn.microsoft.com/37e8f940-617d-43f6-92bd-aadccafe0059">Synchronizing DVD Commands</a>. (This topic also discusses other ways to synchronize commands without using synchronization objects.)




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvdCmd</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvdCmd</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvdCmd</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7dc3113-616a-49d5-bcab-7ed5aa520b18">WaitForEnd</a>
</td>
<td align="left" width="63%">
Blocks the DVD Navigator until the command associated with this object completes or is canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7badcc93-b5e7-4f43-bd71-a0b9ddfb0053">WaitForStart</a>
</td>
<td align="left" width="63%">
Blocks the DVD Navigator until the command associated with this object begins.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/37e8f940-617d-43f6-92bd-aadccafe0059">Synchronizing DVD Commands</a>
 

 


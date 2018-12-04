---
UID: NN:strmif.IAMVfwCompressDialogs
title: IAMVfwCompressDialogs
author: windows-sdk-content
description: The IAMVfwCompressDialogs interface displays a dialog box provided by a Video for Windows (VFW) codec.
old-location: dshow\iamvfwcompressdialogs.htm
tech.root: DirectShow
ms.assetid: 5cc23d68-e0e6-401a-8d16-63c8c68af241
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IAMVfwCompressDialogs, IAMVfwCompressDialogs interface [DirectShow], IAMVfwCompressDialogs interface [DirectShow],described, IAMVfwCompressDialogsInterface, dshow.iamvfwcompressdialogs, strmif/IAMVfwCompressDialogs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVfwCompressDialogs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVfwCompressDialogs interface


## -description



The <code>IAMVfwCompressDialogs</code> interface displays a dialog box provided by a Video for Windows (VFW) codec. The <a href="https://msdn.microsoft.com/addde51d-2982-4964-b16a-406fea89a0ce">AVI Compressor</a> filter implements this interface. Applications can use it to display one of the dialog boxes (Configure or About) provided by VFW codecs, and to set and retrieve compressor status.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMVfwCompressDialogs</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMVfwCompressDialogs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMVfwCompressDialogs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a010fd8a-ad4a-4b52-abfe-a2db8cd15b65">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the current configuration settings for the VCM codec currently being used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1558888-a8aa-416a-bb5b-a33a66dcb913">SendDriverMessage</a>
</td>
<td align="left" width="63%">
Sends a driver-specific message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b27bbaa-4e2f-4567-a6fc-62fb3f5f31a8">SetState</a>
</td>
<td align="left" width="63%">
Sets configuration for the VCM codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4826bd47-0091-4a74-b88d-72a5b0f1c5ac">ShowDialog</a>
</td>
<td align="left" width="63%">
Displays the specified dialog box.

</td>
</tr>
</table> 


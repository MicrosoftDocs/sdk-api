---
UID: NN:windowsstoragecom.IRandomAccessStreamFileAccessMode
title: IRandomAccessStreamFileAccessMode
author: windows-sdk-content
description: Provides access to the file access mode that was used when the StorageFile.OpenAsync method was called to open the random-access byte stream.
old-location: winrt\irandomaccessstreamfileaccessmode.htm
tech.root: WinRT
ms.assetid: 20A538B5-ACD6-4BD9-9CDC-3F2CCDCAF251
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IRandomAccessStreamFileAccessMode, IRandomAccessStreamFileAccessMode interface [Windows Runtime], IRandomAccessStreamFileAccessMode interface [Windows Runtime],described, windowsstoragecom/IRandomAccessStreamFileAccessMode, winrt.irandomaccessstreamfileaccessmode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: windowsstoragecom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.dll: Windows.storage.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.storage.dll
api_name:
 - IRandomAccessStreamFileAccessMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRandomAccessStreamFileAccessMode interface


## -description


Provides access to the file access mode that was used when the <a href="https://msdn.microsoft.com/128318b6-ddfb-44d0-9fcb-80410ad284bf">StorageFile.OpenAsync</a> method was called to open the random-access byte stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRandomAccessStreamFileAccessMode</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRandomAccessStreamFileAccessMode</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRandomAccessStreamFileAccessMode</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F542C4E4-5B65-4909-AF08-C129297A1085">GetMode</a>
</td>
<td align="left" width="63%">
Retrieves the file access mode that was used when the <a href="https://msdn.microsoft.com/128318b6-ddfb-44d0-9fcb-80410ad284bf">StorageFile.OpenAsync</a> method was called to open the random-access byte stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/D2ECEB3D-D13E-44C1-BFE2-1AA57F7432C6">IRandomAccessStream</a>



<a href="https://msdn.microsoft.com/128318b6-ddfb-44d0-9fcb-80410ad284bf">StorageFile.OpenAsync</a>
 

 


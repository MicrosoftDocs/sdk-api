---
UID: NN:mfmediaengine.IMFSourceBufferList
title: IMFSourceBufferList
author: windows-sdk-content
description: Represents a collection of IMFSourceBuffer objects.
old-location: mf\imfsourcebufferlist.htm
tech.root: medfound
ms.assetid: 26f66c2d-5f84-485f-bc86-c8399666c9f1
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFSourceBufferList, IMFSourceBufferList interface [Media Foundation], IMFSourceBufferList interface [Media Foundation],described, mf.imfsourcebufferlist, mfmediaengine/IMFSourceBufferList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - mfmediaengine.h
api_name:
 - IMFSourceBufferList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSourceBufferList interface


## -description


Represents a collection of <a href="https://msdn.microsoft.com/f241e232-9013-46d0-be97-2d6b5246cff3">IMFSourceBuffer</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceBufferList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSourceBufferList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSourceBufferList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/551d2f40-85ad-45af-9191-9fb2b2c44913">GetLength</a>
</td>
<td align="left" width="63%">
Gets the number of <a href="https://msdn.microsoft.com/f241e232-9013-46d0-be97-2d6b5246cff3">IMFSourceBuffer</a> objects  in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f756c2e-79d0-400b-a84a-bc0e268f4f5b">GetSourceBuffer</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/f241e232-9013-46d0-be97-2d6b5246cff3">IMFSourceBuffer</a> at the specified index in the list.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 


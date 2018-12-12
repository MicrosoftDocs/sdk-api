---
UID: NN:control.IBasicVideo2
title: IBasicVideo2
author: windows-sdk-content
description: The IBasicVideo2 interface extends the IBasicVideo interface.
old-location: dshow\ibasicvideo2.htm
tech.root: DirectShow
ms.assetid: a21fe7b9-75db-4c5b-bb29-42d305f048a1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBasicVideo2, IBasicVideo2 interface [DirectShow], IBasicVideo2 interface [DirectShow],described, IBasicVideo2Interface, control/IBasicVideo2, dshow.ibasicvideo2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: control.h
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
 - IBasicVideo2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBasicVideo2 interface


## -description



The <code>IBasicVideo2</code> interface extends the <a href="https://msdn.microsoft.com/en-us/library/Dd389540(v=VS.85).aspx">IBasicVideo</a> interface. The <a href="https://msdn.microsoft.com/7719ed9d-e3b9-4c84-b587-4e120b5cabf8">Video Renderer</a> filter and Video Mixing Renderer filters implement this interface, but the interface is exposed to applications through the Filter Graph Manager. Applications should always retrieve this interface from the Filter Graph Manager.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBasicVideo2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd389540(v=VS.85).aspx">IBasicVideo</a>. <b>IBasicVideo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBasicVideo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd389551(v=VS.85).aspx">GetPreferredAspectRatio</a>
</td>
<td align="left" width="63%">
Retrieves the preferred video aspect ratio.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd389540(v=VS.85).aspx">IBasicVideo</a>
 

 


---
UID: NN:encdec.IXDSCodecConfig
title: IXDSCodecConfig
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005. The IXDSCodecConfig interface configures the XDS Codec filter. Most applications will not have to use this interface.
old-location: mstv\ixdscodecconfig.htm
old-project: mstv
ms.assetid: 90f8ce9b-2a85-43d0-9f2a-a3d248414a2d
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IXDSCodecConfig, IXDSCodecConfig interface [Microsoft TV Technologies], IXDSCodecConfig interface [Microsoft TV Technologies],described, IXDSCodecConfigInterface, encdec/IXDSCodecConfig, mstv.ixdscodecconfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: ProtType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - encdec.h
api_name:
 - IXDSCodecConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IXDSCodecConfig interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>IXDSCodecConfig</b> interface configures the <a href="https://msdn.microsoft.com/5b04314e-76e4-48af-911f-707a5db2100c">XDS Codec</a> filter. Most applications will not have to use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXDSCodecConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXDSCodecConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXDSCodecConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7bf4efe-110a-4bcc-927c-f5e4798211df">GetSecureChannelObject</a>
</td>
<td align="left" width="63%">
Retrieves the secure channel object used to decrypt the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46e71958-86bc-4649-a401-b16131dd6bbd">SetPauseBufferTime</a>
</td>
<td align="left" width="63%">
Specifies how often the XDS Codec filter attempts to generate a new license.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IXDSCodecConfig)</code>.




## -see-also




<a href="https://msdn.microsoft.com/abe939a3-5f43-4fdf-9d4d-34b7be8893eb">TV Ratings Interfaces</a>
 

 


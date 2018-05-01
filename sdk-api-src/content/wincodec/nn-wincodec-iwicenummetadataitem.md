---
UID: NN:wincodec.IWICEnumMetadataItem
title: IWICEnumMetadataItem
author: windows-driver-content
description: Exposes methods that provide enumeration services for individual metadata items.
old-location: wic\_wic_codec_iwicenummetadataitem.htm
old-project: wic
ms.assetid: 4fe0e47f-9ef4-4aa1-a3ae-578b3759f9ef
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IWICEnumMetadataItem, IWICEnumMetadataItem interface [Windows Imaging Component], IWICEnumMetadataItem interface [Windows Imaging Component], described, _wic_codec_iwicenummetadataitem, wic._wic_codec_iwicenummetadataitem, wincodec/IWICEnumMetadataItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICEnumMetadataItem
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICEnumMetadataItem interface


## -description


Exposes methods that provide enumeration services for individual metadata items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICEnumMetadataItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICEnumMetadataItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICEnumMetadataItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the current <b>IWICEnumMetadataItem</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Advanced the current position in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the current position to the beginning of the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips to given number of objects.

</td>
</tr>
</table> 


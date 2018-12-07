---
UID: NN:wmcodecdsp.IWMCodecStrings
title: IWMCodecStrings
author: windows-sdk-content
description: Retrieves names and descriptive strings for codecs and formats.
old-location: mf\iwmcodecstringsinterface.htm
tech.root: medfound
ms.assetid: 84b6223e-d42a-47b0-8553-2b4d69de2da3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMCodecStrings, IWMCodecStrings interface [Media Foundation], IWMCodecStrings interface [Media Foundation],described, codecapi.iwmcodecstringsinterface, mf.iwmcodecstringsinterface, wmcodecdsp/IWMCodecStrings
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmcodecdsp.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMCodecStrings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMCodecStrings interface


## -description


Retrieves names and descriptive strings for codecs and formats.

This interface is implemented by all of the codec encoder objects. You can retrieve a pointer to the <b>IWMCodecStrings</b> interface for any encoder by calling the <b>QueryInterface</b> method of any other interface on the object, such as <a href="https://msdn.microsoft.com/a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b">IMediaObject</a> or <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>, This interface is not implemented on any of the decoder DMOs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMCodecStrings</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMCodecStrings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMCodecStrings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79068e6c-bd16-45e4-a8af-6a03e0c5b528">GetDescription</a>
</td>
<td align="left" width="63%">
Retrieves the description of an output format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12422e46-dfde-4a0f-8988-567a42f5a212">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a codec.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 


---
UID: NN:dvbsiparser.IIsdbLogoTransmissionDescriptor
title: IIsdbLogoTransmissionDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor.
old-location: mstv\iisdblogotransmissiondescriptor.htm
tech.root: mstv
ms.assetid: 9c0930f6-6c05-48c9-91e4-2abdd3355a32
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IIsdbLogoTransmissionDescriptor, IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies], IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbLogoTransmissionDescriptor, mstv.iisdblogotransmissiondescriptor
ms.topic: interface
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - dvbsiparser.h
api_name:
 - IIsdbLogoTransmissionDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbLogoTransmissionDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor. The logo transmission descriptor appears in the ISDB Service Information as part of the service description table (SDT) and contains information required for transmission of logos.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbLogoTransmissionDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsdbLogoTransmissionDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbLogoTransmissionDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3672458d-0f7d-4264-8362-2ddad3afecab">GetDownloadDataId</a>
</td>
<td align="left" width="63%">
Gets the identifier for the downloaded data from an ISDB logo transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f3a29c1-44a4-4513-bab9-2cb77abe0419">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of  an ISDB logo transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb4ba9f1-f633-4cb4-adc4-6671bb5fc239">GetLogoCharW</a>
</td>
<td align="left" width="63%">
Gets the character string for a simple logo from an ISDB logo transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4c11012-5d37-4d8f-944b-edfa50719b12">GetLogoId</a>
</td>
<td align="left" width="63%">
 Gets the logo identifier from an ISDB logo transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8f824ec-36f7-4af0-bce3-295b8403e431">GetLogoTransmissionType</a>
</td>
<td align="left" width="63%">
Gets the logo transmission type from an ISDB logo transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6cc23b4-b0cf-410c-9c15-03d58e795e6b">GetLogoVersion</a>
</td>
<td align="left" width="63%">
 Gets the version number for a logo from an ISDB logo transmission descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ad7d7b5-a20f-4d03-b699-a39fe7ea7568">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB logo transmission descriptor.

</td>
</tr>
</table> 


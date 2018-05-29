---
UID: NN:encdec.IXDSCodec
title: IXDSCodec
author: windows-sdk-content
description: The IXDSCodec interface is exposed by the XDS Codec filter. Most applications will not have to use this interface.
old-location: mstv\ixdscodec.htm
old-project: mstv
ms.assetid: c34a3418-2ae5-45a6-9e3b-2bd7cf33d44b
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IXDSCodec, IXDSCodec interface [Microsoft TV Technologies], IXDSCodec interface [Microsoft TV Technologies],described, IXDSCodecInterface, encdec/IXDSCodec, mstv.ixdscodec
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.typenames: ProtType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EncDec.h
api_name:
-	IXDSCodec
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IXDSCodec interface


## -description



The <b>IXDSCodec</b> interface is exposed by the <a href="https://msdn.microsoft.com/5b04314e-76e4-48af-911f-707a5db2100c">XDS Codec</a> filter. Most applications will not have to use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXDSCodec</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXDSCodec</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXDSCodec</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60523c2c-0d57-46d7-8ab2-eaf065a440d4">get_CCSubstreamService</a>
</td>
<td align="left" width="63%">
Queries which line 21 data channels the XDS Codec filter sends to the <a href="https://msdn.microsoft.com/bda34c12-0eb8-4d3a-867e-f7215f70c7c7">XDSToRat</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/846f3f68-8745-416d-9f0e-1e6ef83054b2">get_XDSToRatObjOK</a>
</td>
<td align="left" width="63%">
Queries whether the <a href="https://msdn.microsoft.com/bda34c12-0eb8-4d3a-867e-f7215f70c7c7">XDSToRat</a> object was created successfully.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/725e444c-ecf4-49da-a800-cc3faf627eea">GetContentAdvisoryRating</a>
</td>
<td align="left" width="63%">
Retrieves the most recent ratings information parsed by the <a href="https://msdn.microsoft.com/bda34c12-0eb8-4d3a-867e-f7215f70c7c7">XDSToRat</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d948df6-6cdf-4283-a2af-3acd47937889">GetCurrLicenseExpDate</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57fd833a-00cc-41d5-acf9-6b07aa8dc115">GetLastErrorCode</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44a74489-4ed7-42f0-b8d5-bf86e0f7072c">GetXDSPacket</a>
</td>
<td align="left" width="63%">
Retrieves the most recent XDS packet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8e4a43a-3e9f-468a-8df3-7ff05d23b20b">put_CCSubstreamService</a>
</td>
<td align="left" width="63%">
Specifies which line 21 data channels the XDS Codec filter sends to the <a href="https://msdn.microsoft.com/bda34c12-0eb8-4d3a-867e-f7215f70c7c7">XDSToRat</a> object.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IXDSCodec)</code>.




## -see-also




<a href="https://msdn.microsoft.com/abe939a3-5f43-4fdf-9d4d-34b7be8893eb">TV Ratings Interfaces</a>
 

 


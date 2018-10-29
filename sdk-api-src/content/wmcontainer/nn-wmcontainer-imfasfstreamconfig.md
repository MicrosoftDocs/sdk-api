---
UID: NN:wmcontainer.IMFASFStreamConfig
title: IMFASFStreamConfig
author: windows-sdk-content
description: Configures the settings of a stream in an ASF file.
old-location: mf\imfasfstreamconfig.htm
tech.root: medfound
ms.assetid: 7bb63396-21c2-400d-b9de-c00b90f46d62
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 7bb63396-21c2-400d-b9de-c00b90f46d62, IMFASFStreamConfig, IMFASFStreamConfig interface [Media Foundation], IMFASFStreamConfig interface [Media Foundation],described, mf.imfasfstreamconfig, wmcontainer/IMFASFStreamConfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFStreamConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFStreamConfig interface


## -description


Configures the settings of a stream in an ASF file. The ASF stream configuration object exposes this interface. To obtain a pointer to this interface, call the <a href="https://msdn.microsoft.com/3da52c1a-24c0-456b-a9e8-57b5467eda2a">IMFASFProfile::CreateStream</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFASFStreamConfig</b> interface inherits from <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>. <b>IMFASFStreamConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFASFStreamConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55dd4125-ce44-4eed-b1a8-74819c452bd4">AddPayloadExtension</a>
</td>
<td align="left" width="63%">
Configures a payload extension for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c87d658f-6569-464b-a9d0-487d44f76cc0">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the ASF stream configuration object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6311115a-26e6-47b7-b724-0209a5bf45d7">GetMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the media type of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b3b831c-2218-4a76-8359-7f39cab53a57">GetPayloadExtension</a>
</td>
<td align="left" width="63%">
Retrieves information about an existing payload extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b1cb5a9-e39c-4f16-abc1-45ab516a4b80">GetPayloadExtensionCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of payload extensions that are configured for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc80fee6-e62c-4d38-9b83-8c7f21baf5b0">GetStreamNumber</a>
</td>
<td align="left" width="63%">
Retrieves the stream number of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f085107-f205-47ab-acb5-d45a881ce76c">GetStreamType</a>
</td>
<td align="left" width="63%">
Retrieves the major media type of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b2c592b-28f6-49a9-9bf5-1080202f606a">RemoveAllPayloadExtensions</a>
</td>
<td align="left" width="63%">
Removes all payload extensions that are configured for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53b7c4fd-a3bc-4e15-b2f6-380cae8ab2f6">SetMediaType</a>
</td>
<td align="left" width="63%">
Sets the media type for the ASF stream configuration object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b22d857-fced-4094-a0ad-891f3ccf8b18">SetStreamNumber</a>
</td>
<td align="left" width="63%">
Assigns a stream number to the stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 


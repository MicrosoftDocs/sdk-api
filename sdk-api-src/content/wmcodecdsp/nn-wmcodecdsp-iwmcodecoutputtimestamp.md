---
UID: NN:wmcodecdsp.IWMCodecOutputTimestamp
title: IWMCodecOutputTimestamp
author: windows-sdk-content
description: Gets the time stamp of the next video frame to be decoded.
old-location: mf\iwmcodecoutputtimestampinterface.htm
old-project: medfound
ms.assetid: 0dbac3fa-7521-434d-aa0a-2e8422c3da59
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IWMCodecOutputTimestamp, IWMCodecOutputTimestamp interface [Media Foundation], IWMCodecOutputTimestamp interface [Media Foundation],described, codecapi.iwmcodecoutputtimestampinterface, mf.iwmcodecoutputtimestampinterface, wmcodecdsp/IWMCodecOutputTimestamp
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFVideoDSPMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMCodecOutputTimestamp
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMCodecOutputTimestamp interface


## -description


Gets the time stamp of the  next video frame to be decoded.

This interface is implemented by the video decoders. You can obtain a pointer to <b>IWMCodecOutputTimestamp</b> by calling the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method of any other interface of the decoder object, such as <a href="https://msdn.microsoft.com/a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b">IMediaObject</a> or <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMCodecOutputTimestamp</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMCodecOutputTimestamp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMCodecOutputTimestamp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8af7e77b-da10-4d6a-b7a1-515a54aa3a20">GetNextOutputTime</a>
</td>
<td align="left" width="63%">
Retrieves the time stamp of the next video frame to be decoded.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/897b8e2d-9827-428d-91ae-632038c4c8c0">Configuring Video Decoding</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 


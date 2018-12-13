---
UID: NN:wincodecsdk.IWICPersistStream
title: IWICPersistStream
author: windows-sdk-content
description: Exposes methods that provide additional load and save methods that take WICPersistOptions.
old-location: wic\_wic_codec_iwicpersiststream.htm
tech.root: wic
ms.assetid: 9381cc2c-9554-4071-b9b5-3464d857c02d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWICPersistStream, IWICPersistStream interface [Windows Imaging Component], IWICPersistStream interface [Windows Imaging Component],described, _wic_codec_iwicpersiststream, wic._wic_codec_iwicpersiststream, wincodecsdk/IWICPersistStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICPersistStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICPersistStream interface


## -description


Exposes methods that provide additional load and save methods that take <a href="https://msdn.microsoft.com/8c17cfcc-4f09-4cb5-a3fa-4eb865123ad6">WICPersistOptions</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICPersistStream</b> interface inherits from <a href="d47b175c-7054-42af-ae1a-9a350ead867c">IPersistStream</a>. <b>IWICPersistStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICPersistStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb200a21-6c01-469e-b70f-f787f1dae382">LoadEx</a>
</td>
<td align="left" width="63%">
Loads a stream using the given parameters. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8820ad87-a808-48db-91d8-c76bca1c832c">SaveEx</a>
</td>
<td align="left" width="63%">
Saves the stream using the given parameters.

</td>
</tr>
</table> 


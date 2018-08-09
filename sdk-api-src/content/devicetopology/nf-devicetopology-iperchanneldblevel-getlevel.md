---
UID: NF:devicetopology.IPerChannelDbLevel.GetLevel
title: IPerChannelDbLevel::GetLevel
author: windows-sdk-content
description: The GetLevel method gets the volume level, in decibels, of the specified channel.
old-location: coreaudio\iperchanneldblevel_getlevel.htm
old-project: CoreAudio
ms.assetid: afc76c80-1656-4f06-8024-c9b041f52e64
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetLevel, GetLevel method [Core Audio], GetLevel method [Core Audio],IPerChannelDbLevel interface, IPerChannelDbLevel interface [Core Audio],GetLevel method, IPerChannelDbLevel.GetLevel, IPerChannelDbLevel::GetLevel, IPerChannelDbLevelGetLevel, coreaudio.iperchanneldblevel_getlevel, devicetopology/IPerChannelDbLevel::GetLevel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: devicetopology.h
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
tech.root: 
req.typenames: ConnectorType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IPerChannelDbLevel.GetLevel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IPerChannelDbLevel::GetLevel


## -description



The <b>GetLevel</b> method gets the volume level, in decibels, of the specified channel.




## -parameters




### -param nChannel [in]

The channel number. If the audio stream has <i>N</i> channels, the channels are numbered from 0 to <i>N</i>– 1. To get the number of channels in the stream, call the <a href="https://msdn.microsoft.com/f8c6c0fd-fe29-467a-936e-f83c6d951bdd">IPerChannelDbLevel::GetChannelCount</a> method.


### -param pfLevelDB [out]

Pointer to a <b>float</b> variable into which the method writes the volume level, in decibels, of the specified channel.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>nChannel</i> is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pfLevelDB</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e70b4518-c9de-4426-b8e5-db80656699a9">IPerChannelDbLevel Interface</a>



<a href="https://msdn.microsoft.com/f8c6c0fd-fe29-467a-936e-f83c6d951bdd">IPerChannelDbLevel::GetChannelCount</a>
 

 


---
UID: NF:devicetopology.IPerChannelDbLevel.GetLevelRange
title: IPerChannelDbLevel::GetLevelRange
author: windows-sdk-content
description: The GetLevelRange method gets the range, in decibels, of the volume level of the specified channel.
old-location: coreaudio\iperchanneldblevel_getlevelrange.htm
old-project: CoreAudio
ms.assetid: 492eddb0-f8f2-4639-b5fe-1d02bf8c983a
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetLevelRange, GetLevelRange method [Core Audio], GetLevelRange method [Core Audio],IPerChannelDbLevel interface, IPerChannelDbLevel interface [Core Audio],GetLevelRange method, IPerChannelDbLevel.GetLevelRange, IPerChannelDbLevel::GetLevelRange, IPerChannelDbLevelGetLevelRange, coreaudio.iperchanneldblevel_getlevelrange, devicetopology/IPerChannelDbLevel::GetLevelRange
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
 - IPerChannelDbLevel.GetLevelRange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IPerChannelDbLevel::GetLevelRange


## -description



The <b>GetLevelRange</b> method gets the range, in decibels, of the volume level of the specified channel.




## -parameters




### -param nChannel [in]

The number of the selected channel. If the audio stream has <i>n</i> channels, the channels are numbered from 0 to <i>n</i>– 1. To get the number of channels in the stream, call the <a href="https://msdn.microsoft.com/f8c6c0fd-fe29-467a-936e-f83c6d951bdd">IPerChannelDbLevel::GetChannelCount</a> method.


### -param pfMinLevelDB [out]

Pointer to a <b>float</b> variable into which the method writes the minimum volume level in decibels.


### -param pfMaxLevelDB [out]

Pointer to a <b>float</b> variable into which the method writes the maximum volume level in decibels.


### -param pfStepping [out]

Pointer to a <b>float</b> variable into which the method writes the stepping value between consecutive volume levels in the range  <i>*pfMinLevelDB</i> to  <i>*pfMaxLevelDB</i>. If the difference between the maximum and minimum volume levels is <i>d</i> decibels, and the range is divided into <i>n</i> steps (uniformly sized intervals), then the volume can have <i>n</i> + 1 discrete levels and the size of the step between consecutive levels is <i>d</i> / <i>n</i> decibels.


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
Pointer <i>pfminLevelDB</i>, <i>pfmaxLevelDB</i>, or <i>pfmaxLevelDB</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e70b4518-c9de-4426-b8e5-db80656699a9">IPerChannelDbLevel Interface</a>



<a href="https://msdn.microsoft.com/f8c6c0fd-fe29-467a-936e-f83c6d951bdd">IPerChannelDbLevel::GetChannelCount</a>
 

 


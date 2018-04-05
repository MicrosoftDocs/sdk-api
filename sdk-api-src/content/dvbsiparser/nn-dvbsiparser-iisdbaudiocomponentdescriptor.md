---
UID: NN:dvbsiparser.IIsdbAudioComponentDescriptor
title: IIsdbAudioComponentDescriptor
author: windows-driver-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor.
old-location: mstv\iisdbaudiocomponentdescriptor.htm
old-project: mstv
ms.assetid: f771b318-5fd5-4c7f-a22b-6966aec5c0fa
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IIsdbAudioComponentDescriptor, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies], IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies], described, dvbsiparser/IIsdbAudioComponentDescriptor, mstv.iisdbaudiocomponentdescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbAudioComponentDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbAudioComponentDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. The audio component descriptor appears in the ISDB service information as part of the event information table (EIT) and provides information about the audio.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbAudioComponentDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsdbAudioComponentDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbAudioComponentDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b06f566-b5e0-43c8-8694-24d913bbf971">GetComponentTag</a>
</td>
<td align="left" width="63%">
 Gets the component tag from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/417deb6e-863e-4d62-8d58-685972f96f0c">GetComponentType</a>
</td>
<td align="left" width="63%">
Gets the component type from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10a47ca7-84db-48de-8ba5-0be257438044">GetESMultiLingualFlag</a>
</td>
<td align="left" width="63%">
 Gets the ES multilingual flag from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f44f9c6-7eb6-4c4d-b25b-b2a95dcaa658">GetLanguageCode</a>
</td>
<td align="left" width="63%">
 Gets the three-character ISO 639 language code
or, in ES multilingual mode, gets the first language code from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3016264e-c952-4243-acd2-a075c89e8c2b">GetLanguageCode2</a>
</td>
<td align="left" width="63%">
In ES multilingual mode, gets the second  three-character ISO 639 language code from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3e2f0f8-7e06-43fd-94c2-da54ea5a761b">GetLength</a>
</td>
<td align="left" width="63%">
  Gets the body length of an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/223bb5d2-2b19-44e7-a347-16b2930f00a6">GetMainComponentFlag</a>
</td>
<td align="left" width="63%">
Gets a flag indicating the main audio component from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39d85ecd-6ccd-48e8-9498-41aad45a7357">GetQualityIndicator</a>
</td>
<td align="left" width="63%">
 Gets a code indicating the tone quality mode from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccb31b56-10a1-47ee-9d1b-116d860bef11">GetSamplingRate</a>
</td>
<td align="left" width="63%">
 Gets the sampling rate from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/125fa9c2-eba0-497b-82ca-cc3223e40b44">GetSimulcastGroupTag</a>
</td>
<td align="left" width="63%">
 Gets the simulcast group tag from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1283c029-d1f5-4da8-a0fe-c795b4cd093c">GetStreamContent</a>
</td>
<td align="left" width="63%">
 Gets the stream content from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73c7a8c8-7098-43e8-ac90-c29586e9856c">GetStreamType</a>
</td>
<td align="left" width="63%">
 Gets the stream type from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b44ef442-3bfc-4b1f-b64d-4be21fc1fb47">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/beeb31dd-28f8-45bb-bda0-0dbf6bca679b">GetTextW</a>
</td>
<td align="left" width="63%">
 Gets the component stream description from an ISDB audio component descriptor, in Unicode text format.


</td>
</tr>
</table> 


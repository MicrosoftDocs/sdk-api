---
UID: NN:dvbsiparser.IIsdbAudioComponentDescriptor
title: IIsdbAudioComponentDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor.
old-location: mstv\iisdbaudiocomponentdescriptor.htm
tech.root: mstv
ms.assetid: f771b318-5fd5-4c7f-a22b-6966aec5c0fa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IIsdbAudioComponentDescriptor, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies], IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbAudioComponentDescriptor, mstv.iisdbaudiocomponentdescriptor
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IIsdbAudioComponentDescriptor"
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
 - IIsdbAudioComponentDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbAudioComponentDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. The audio component descriptor appears in the ISDB service information as part of the event information table (EIT) and provides information about the audio.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbAudioComponentDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbAudioComponentDescriptor</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbaudiocomponentdescriptor-getcomponenttag">GetComponentTag</a>
</td>
<td align="left" width="63%">
 Gets the component tag from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbaudiocomponentdescriptor-getcomponenttype">GetComponentType</a>
</td>
<td align="left" width="63%">
Gets the component type from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbaudiocomponentdescriptor-getesmultilingualflag">GetESMultiLingualFlag</a>
</td>
<td align="left" width="63%">
 Gets the ES multilingual flag from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbaudiocomponentdescriptor-getlanguagecode">GetLanguageCode</a>
</td>
<td align="left" width="63%">
 Gets the three-character ISO 639 language code
or, in ES multilingual mode, gets the first language code from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbaudiocomponentdescriptor-getlanguagecode2">GetLanguageCode2</a>
</td>
<td align="left" width="63%">
In ES multilingual mode, gets the second  three-character ISO 639 language code from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbaudiocomponentdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
  Gets the body length of an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbaudiocomponentdescriptor-getmaincomponentflag">GetMainComponentFlag</a>
</td>
<td align="left" width="63%">
Gets a flag indicating the main audio component from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbaudiocomponentdescriptor-getqualityindicator">GetQualityIndicator</a>
</td>
<td align="left" width="63%">
 Gets a code indicating the tone quality mode from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbaudiocomponentdescriptor-getsamplingrate">GetSamplingRate</a>
</td>
<td align="left" width="63%">
 Gets the sampling rate from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbaudiocomponentdescriptor-getsimulcastgrouptag">GetSimulcastGroupTag</a>
</td>
<td align="left" width="63%">
 Gets the simulcast group tag from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbaudiocomponentdescriptor-getstreamcontent">GetStreamContent</a>
</td>
<td align="left" width="63%">
 Gets the stream content from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbaudiocomponentdescriptor-getstreamtype">GetStreamType</a>
</td>
<td align="left" width="63%">
 Gets the stream type from an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbaudiocomponentdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB audio component descriptor.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbaudiocomponentdescriptor-gettextw">GetTextW</a>
</td>
<td align="left" width="63%">
 Gets the component stream description from an ISDB audio component descriptor, in Unicode text format.


</td>
</tr>
</table> 


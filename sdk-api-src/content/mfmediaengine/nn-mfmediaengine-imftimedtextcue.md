---
UID: NN:mfmediaengine.IMFTimedTextCue
title: IMFTimedTextCue
author: windows-sdk-content
description: Represents the timed-text-cue object.
old-location: mf\imftimedtextcue.htm
tech.root: medfound
ms.assetid: 831FA230-D0C4-4115-8447-D882686D80EE
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IMFTimedTextCue, IMFTimedTextCue interface [Media Foundation], IMFTimedTextCue interface [Media Foundation],described, mf.imftimedtextcue, mfmediaengine/IMFTimedTextCue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - mfmediaengine.h
api_name:
 - IMFTimedTextCue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextCue interface


## -description


Represents the timed-text-cue object. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTimedTextCue</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTimedTextCue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTimedTextCue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1BEB539D-4A51-4866-A627-5754525E7C8F">GetCueKind</a>
</td>
<td align="left" width="63%">
Gets the kind of timed-text cue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18884B70-DE34-494E-A029-6DD48AB0BA13">GetData</a>
</td>
<td align="left" width="63%">
Gets the data content of the timed-text cue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6E2CD435-C628-4F8B-B648-9EEBCFDA8EC2">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the duration time of the cue in the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D096B1FA-E92F-4B09-9177-13203FF1704D">GetId</a>
</td>
<td align="left" width="63%">
Gets the identifier of a timed-text cue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CD29A63D-8D40-43E6-972C-7050E63EA7D3">GetLine</a>
</td>
<td align="left" width="63%">
Gets a line of text in the cue from the index of the line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5930C8BB-5F00-4263-B3F6-B61EF6DBD0DA">GetLineCount</a>
</td>
<td align="left" width="63%">
Gets the number of lines of text in the timed-text cue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D5B94171-AEB0-4A7D-B596-F888B69A436D">GetOriginalId</a>
</td>
<td align="left" width="63%">
Gets the cue identifier that is provided in the text-track data format, if available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8F5CE96E-9714-4F1A-8CB5-87FA24735B9D">GetRegion</a>
</td>
<td align="left" width="63%">
Gets info about the display region  of the timed-text cue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A5D7766E-7692-449A-86CE-93A787DBDCDC">GetStartTime</a>
</td>
<td align="left" width="63%">
Gets the start time of the cue in the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9E0B570D-69AA-449D-9988-96632A52756F">GetStyle</a>
</td>
<td align="left" width="63%">
Gets info about the style  of the timed-text cue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/967CA2AC-A36A-4875-9882-6EF4748EC92C">GetTrackId</a>
</td>
<td align="left" width="63%">
Gets the identifier of the timed-text cue.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 


---
UID: NN:mfidl.IMFRateSupport
title: IMFRateSupport
author: windows-sdk-content
description: Queries the range of playback rates that are supported, including reverse playback.
old-location: mf\imfratesupport.htm
tech.root: medfound
ms.assetid: a6c495fa-0f6a-4e4c-8fba-996b22d55053
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFRateSupport, IMFRateSupport interface [Media Foundation], IMFRateSupport interface [Media Foundation],described, a6c495fa-0f6a-4e4c-8fba-996b22d55053, mf.imfratesupport, mfidl/IMFRateSupport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFRateSupport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFRateSupport interface


## -description


Queries the range of playback rates that are supported, including reverse playback.

To get a pointer to this interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> with the service identifier MF_RATE_CONTROL_SERVICE.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFRateSupport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFRateSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFRateSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00413771-21cb-48a7-9080-2c3d195c366b">GetFastestRate</a>
</td>
<td align="left" width="63%">
Gets the fastest playback rate supported by the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e10125e9-8bc7-4fb6-8a10-ba5717f1596f">GetSlowestRate</a>
</td>
<td align="left" width="63%">
Gets the slowest playback rate supported by the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ac04683-17d3-4d87-b260-39b04eab9e59">IsRateSupported</a>
</td>
<td align="left" width="63%">
Queries whether the object supports a specified playback rate.

</td>
</tr>
</table> 


## -remarks



Applications can use this interface to discover the fastest and slowest playback rates that are possible, and to query whether a given playback rate is supported. Applications obtain this interface from the Media Session. Internally, the Media Session queries the objects in the pipeline. For more information, see <a href="https://msdn.microsoft.com/7f2b64e1-1062-4f77-b8e0-62b6d962ae8b">How to Determine Supported Rates</a>.

To get the current playback rate and to change the playback rate, use the <a href="https://msdn.microsoft.com/54303c32-b260-4364-9130-a592694f2816">IMFRateControl</a> interface.

Playback rates are expressed as a ratio the normal playback rate. Reverse playback is expressed as a negative rate. Playback is either <i>thinned</i> or <i>non-thinned</i>. In thinned playback, some of the source data is skipped (typically delta frames). In non-thinned playback, all of the source data is rendered.

You might need to implement this interface if you are writing a pipeline object (media source, transform, or media sink). For more information, see <a href="https://msdn.microsoft.com/077678db-ca5a-423b-9430-93497113d639">Implementing Rate Control</a>.




## -see-also




<a href="https://msdn.microsoft.com/54303c32-b260-4364-9130-a592694f2816">IMFRateControl</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 


---
UID: NN:wincodec.IWICDevelopRawNotificationCallback
title: IWICDevelopRawNotificationCallback (wincodec.h)

description: Exposes a callback method for raw image change nofications.
old-location: wic\_wic_codec_iwicdeveloprawnotificationcallback.htm
tech.root: wic
ms.assetid: ccd162e4-84be-4ed5-a583-c9bd195f503b

ms.date: 12/05/2018
ms.keywords: IWICDevelopRawNotificationCallback, IWICDevelopRawNotificationCallback interface [Windows Imaging Component], IWICDevelopRawNotificationCallback interface [Windows Imaging Component],described, _wic_codec_iwicdeveloprawnotificationcallback, wic._wic_codec_iwicdeveloprawnotificationcallback, wincodec/IWICDevelopRawNotificationCallback
ms.topic: interface
f1_keywords: 
 - "wincodec/IWICDevelopRawNotificationCallback"
dev_langs:
 - c++
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
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
 - IWICDevelopRawNotificationCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICDevelopRawNotificationCallback interface


## -description


Exposes a callback method for raw image change nofications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICDevelopRawNotificationCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICDevelopRawNotificationCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICDevelopRawNotificationCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify">Notify</a>
</td>
<td align="left" width="63%">
An application-defined callback method used for raw image parameter change notifications.

</td>
</tr>
</table> 


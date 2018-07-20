---
UID: NN:evr.IMFVideoDeviceID
title: IMFVideoDeviceID
author: windows-sdk-content
description: Returns the device identifier supported by a video renderer component.
old-location: mf\imfvideodeviceid.htm
old-project: medfound
ms.assetid: c42b75f9-6b72-4aab-92f2-3361ab475ce9
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFVideoDeviceID, IMFVideoDeviceID interface [Media Foundation], IMFVideoDeviceID interface [Media Foundation],described, c42b75f9-6b72-4aab-92f2-3361ab475ce9, evr/IMFVideoDeviceID, mf.imfvideodeviceid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: evr.h
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
req.typenames: MFVideoMixPrefs
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoDeviceID
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoDeviceID interface


## -description


Returns the device identifier supported by a video renderer component. This interface is implemented by mixers and presenters for the enhanced video renderer (EVR). If you replace either of these components, the mixer and presenter must report the same device identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoDeviceID</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFVideoDeviceID</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoDeviceID</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e23ebce0-be58-413a-ab71-d94811c96029">GetDeviceID</a>
</td>
<td align="left" width="63%">
Returns the identifier of the video device supported by the EVR mixer or presenter.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 


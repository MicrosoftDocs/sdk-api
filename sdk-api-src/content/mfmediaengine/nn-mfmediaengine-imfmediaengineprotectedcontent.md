---
UID: NN:mfmediaengine.IMFMediaEngineProtectedContent
title: IMFMediaEngineProtectedContent (mfmediaengine.h)
author: windows-sdk-content
description: Enables the Media Engine to play protected video content.
old-location: mf\imfmediaengineprotectedcontent.htm
tech.root: medfound
ms.assetid: 85B37711-DB46-4BC7-A051-79E9507791FA
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineProtectedContent, IMFMediaEngineProtectedContent interface [Media Foundation], IMFMediaEngineProtectedContent interface [Media Foundation],described, mf.imfmediaengineprotectedcontent, mfmediaengine/IMFMediaEngineProtectedContent
ms.topic: interface
f1_keywords: 
 - "mfmediaengine/IMFMediaEngineProtectedContent"
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMFMediaEngineProtectedContent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineProtectedContent interface


## -description


Enables the Media Engine to play protected video content.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineProtectedContent</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEngineProtectedContent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineProtectedContent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-getrequiredprotections">GetRequiredProtections</a>
</td>
<td align="left" width="63%">
Gets the content protections that must be applied in frame-server mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate">SetApplicationCertificate</a>
</td>
<td align="left" width="63%">
Sets the application's certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setcontentprotectionmanager">SetContentProtectionManager</a>
</td>
<td align="left" width="63%">
Sets the content protection manager (CPM).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow">SetOPMWindow</a>
</td>
<td align="left" width="63%">
Specifies the window that should receive output link protections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-shareresources">ShareResources</a>
</td>
<td align="left" width="63%">
Enables the Media Engine to access protected content while in frame-server mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-transfervideoframe">TransferVideoFrame</a>
</td>
<td align="left" width="63%">
Copies a protected video frame to a DXGI surface.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on the Media Engine.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 


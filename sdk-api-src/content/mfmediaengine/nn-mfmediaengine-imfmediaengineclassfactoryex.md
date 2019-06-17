---
UID: NN:mfmediaengine.IMFMediaEngineClassFactoryEx
title: IMFMediaEngineClassFactoryEx (mfmediaengine.h)
author: windows-sdk-content
description: Extension for the IMFMediaEngineClassFactory interface.
old-location: mf\imfmediaengineclassfactoryex.htm
tech.root: medfound
ms.assetid: d672ee59-f702-49c7-8ccf-5ba0260c9b23
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineClassFactoryEx, IMFMediaEngineClassFactoryEx interface [Media Foundation], IMFMediaEngineClassFactoryEx interface [Media Foundation],described, mf.imfmediaengineclassfactoryex, mfmediaengine/IMFMediaEngineClassFactoryEx
ms.topic: interface
f1_keywords: ["mfmediaengine/IMFMediaEngineClassFactoryEx"]
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IMFMediaEngineClassFactoryEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineClassFactoryEx interface


## -description


Extension for the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory">IMFMediaEngineClassFactory</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineClassFactoryEx</b> interface inherits from <b>IMFMediaEngineClassFactory</b>. <b>IMFMediaEngineClassFactoryEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineClassFactoryEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactoryex-createmediakeys">CreateMediaKeys</a>
</td>
<td align="left" width="63%">
Creates a media keys object based on the specified key system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactoryex-createmediasourceextension">CreateMediaSourceExtension</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension">IMFMediaSourceExtension</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfmediaengineclassfactoryex-istypesupported">IsTypeSupported</a>
</td>
<td align="left" width="63%">
Gets a value that indicates if the specified key system supports the specified media type.

</td>
</tr>
</table> 


## -remarks



This class is implemented by the Media Engine (CLSID_MFMediaEngineClassFactory).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 


---
UID: NN:mfmediaengine.IMFMediaEngineClassFactory
title: IMFMediaEngineClassFactory (mfmediaengine.h)

description: Creates an instance of the Media Engine.
old-location: mf\imfmediaengineclassfactory.htm
tech.root: medfound
ms.assetid: 8E4E84A0-BCFC-4CBF-813B-4FEE2B42A83E

ms.date: 12/05/2018
ms.keywords: IMFMediaEngineClassFactory, IMFMediaEngineClassFactory interface [Media Foundation], IMFMediaEngineClassFactory interface [Media Foundation],described, mf.imfmediaengineclassfactory, mfmediaengine/IMFMediaEngineClassFactory
ms.topic: interface
f1_keywords: 
 - "mfmediaengine/IMFMediaEngineClassFactory"
dev_langs:
 - c++
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
 - IMFMediaEngineClassFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineClassFactory interface


## -description


Creates an instance of the Media Engine.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineClassFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEngineClassFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineClassFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createerror">CreateError</a>
</td>
<td align="left" width="63%">
Creates a media error object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates a new instance of the Media Engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createtimerange">CreateTimeRange</a>
</td>
<td align="left" width="63%">
Creates a time range object.

</td>
</tr>
</table> 


## -remarks



Before using this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> and <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a>.

To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>. The class identifier is <b>CLSID_MFMediaEngineClassFactory</b>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=241429">Media Engine Sample</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 


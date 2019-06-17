---
UID: NF:mfmediaengine.IMFMediaEngineClassFactoryEx.CreateMediaSourceExtension
title: IMFMediaEngineClassFactoryEx::CreateMediaSourceExtension (mfmediaengine.h)
author: windows-sdk-content
description: Creates an instance of IMFMediaSourceExtension.
old-location: mf\imfmediaengineclassfactoryex_createmediasourceextension.htm
tech.root: medfound
ms.assetid: 2a76bae3-0b7e-49fe-ab5d-bfb32d029d60
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateMediaSourceExtension, CreateMediaSourceExtension method [Media Foundation], CreateMediaSourceExtension method [Media Foundation],IMFMediaEngineClassFactoryEx interface, IMFMediaEngineClassFactoryEx interface [Media Foundation],CreateMediaSourceExtension method, IMFMediaEngineClassFactoryEx.CreateMediaSourceExtension, IMFMediaEngineClassFactoryEx::CreateMediaSourceExtension, mf.imfmediaengineclassfactoryex_createmediasourceextension, mfmediaengine/IMFMediaEngineClassFactoryEx::CreateMediaSourceExtension
ms.topic: method
f1_keywords: ["mfmediaengine/IMFMediaEngineClassFactoryEx.CreateMediaSourceExtension"]
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
 - IMFMediaEngineClassFactoryEx.CreateMediaSourceExtension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineClassFactoryEx::CreateMediaSourceExtension


## -description


Creates an instance of <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension">IMFMediaSourceExtension</a>.


## -parameters




### -param dwFlags [in]

This parameter is reserved and must be set to 0.


### -param pAttr [in]

This method supports the following  Media Foundation attributes:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-mse-callback">MF_MSE_CALLBACK</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-mse-bufferlist-callback">MF_MSE_BUFFERLIST_CALLBACK</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-mse-activelist-callback">MF_MSE_ACTIVELIST_CALLBACK</a>
</li>
</ul>

### -param ppMSE [out]

The <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension">IMFMediaSourceExtension</a> which was created.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex">IMFMediaEngineClassFactoryEx</a>
 

 


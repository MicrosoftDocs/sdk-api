---
UID: NF:mfmediaengine.IMFMediaEngineProtectedContent.ShareResources
title: IMFMediaEngineProtectedContent::ShareResources (mfmediaengine.h)
description: Enables the Media Engine to access protected content while in frame-server mode.helpviewer_keywords: ["IMFMediaEngineProtectedContent interface [Media Foundation]","ShareResources method","IMFMediaEngineProtectedContent.ShareResources","IMFMediaEngineProtectedContent::ShareResources","ShareResources","ShareResources method [Media Foundation]","ShareResources method [Media Foundation]","IMFMediaEngineProtectedContent interface","mf.imfmediaengineprotectedcontent_shareresources","mfmediaengine/IMFMediaEngineProtectedContent::ShareResources"]
old-location: mf\imfmediaengineprotectedcontent_shareresources.htm
tech.root: medfound
ms.assetid: 7C94AEA2-1D72-4C45-9EDF-90593CC60E2C
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineProtectedContent interface [Media Foundation],ShareResources method, IMFMediaEngineProtectedContent.ShareResources, IMFMediaEngineProtectedContent::ShareResources, ShareResources, ShareResources method [Media Foundation], ShareResources method [Media Foundation],IMFMediaEngineProtectedContent interface, mf.imfmediaengineprotectedcontent_shareresources, mfmediaengine/IMFMediaEngineProtectedContent::ShareResources
f1_keywords:
- mfmediaengine/IMFMediaEngineProtectedContent.ShareResources
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
- IMFMediaEngineProtectedContent.ShareResources
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineProtectedContent::ShareResources


## -description


Enables the Media Engine to access protected content while in frame-server mode.


## -parameters




### -param pUnkDeviceContext [in]

A pointer to the Direct3D 11 device content. The Media Engine queries this pointer for the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a> interface. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In frame-server mode, this method enables the Media Engine to share protected content with the Direct3D 11 device.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineprotectedcontent">IMFMediaEngineProtectedContent</a>
 

 


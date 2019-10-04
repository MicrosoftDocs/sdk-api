---
UID: NF:mfapi.MFCreateMediaExtensionActivate
title: MFCreateMediaExtensionActivate function (mfapi.h)
author: windows-sdk-content
description: Creates an activation object for a Windows Runtime class.
old-location: mf\mfcreatemediaextensionactivate.htm
tech.root: medfound
ms.assetid: 3F9538F2-DB7A-4841-B61D-C59BC02718B1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFCreateMediaExtensionActivate, MFCreateMediaExtensionActivate function [Media Foundation], mf.mfcreatemediaextensionactivate, mf.mfcreatewinrtactivate, mfapi/MFCreateMediaExtensionActivate
ms.topic: function
f1_keywords: 
 - "mfapi/MFCreateMediaExtensionActivate"
dev_langs:
 - c++
req.header: mfapi.h
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateMediaExtensionActivate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateMediaExtensionActivate function


## -description


Creates an activation object for a Windows Runtime class.


## -parameters




### -param szActivatableClassId [in]

The class identifier that is associated with the activatable runtime class.


### -param pConfiguration [in]

A pointer to an optional <a href="https://docs.microsoft.com/en-us/uwp/api/windows.foundation.collections.ipropertyset">IPropertySet</a> object, which is used to configure the Windows Runtime class. This parameter can be <b>NULL</b>.


### -param riid [in]

The interface identifier (IID) of the interface being requested. The activation object created  by this function supports the following interfaces:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>
</li>
</ul>

### -param ppvObject [out]

Receives a pointer to the requested interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To create the Windows Runtime object, call <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a> or <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance">IClassFactory::CreateInstance</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 


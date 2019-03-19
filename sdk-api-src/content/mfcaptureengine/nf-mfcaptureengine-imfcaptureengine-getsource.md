---
UID: NF:mfcaptureengine.IMFCaptureEngine.GetSource
title: IMFCaptureEngine::GetSource (mfcaptureengine.h)
author: windows-sdk-content
description: Gets a pointer to the capture source object.
old-location: mf\imfcaptureengine_getsource.htm
tech.root: medfound
ms.assetid: 9DED11CA-BDBB-4E1A-BAD1-2EB6216543F9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSource, GetSource method [Media Foundation], GetSource method [Media Foundation],IMFCaptureEngine interface, IMFCaptureEngine interface [Media Foundation],GetSource method, IMFCaptureEngine.GetSource, IMFCaptureEngine::GetSource, mf.imfcaptureengine_getsource, mfcaptureengine/IMFCaptureEngine::GetSource
ms.topic: method
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - mfcaptureengine.h
api_name:
 - IMFCaptureEngine.GetSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureEngine::GetSource


## -description


Gets a pointer to the capture source object. Use the capture source to configure the capture devices.


## -parameters




### -param ppSource [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/864B6B5D-EB7E-4C49-A326-9B6704A27635">IMFCaptureSource</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4A2A0536-4255-40AB-BCAB-228B09343583">IMFCaptureEngine</a>
 

 


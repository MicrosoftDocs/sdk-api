---
UID: NN:mfcaptureengine.IMFCaptureEngineClassFactory
title: IMFCaptureEngineClassFactory
author: windows-sdk-content
description: Creates an instance of the capture engine.
old-location: mf\imfcaptureengineclassfactory.htm
tech.root: medfound
ms.assetid: FAFA52AD-B96E-4ADC-BE79-3BE5F1ACC92A
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IMFCaptureEngineClassFactory, IMFCaptureEngineClassFactory interface [Media Foundation], IMFCaptureEngineClassFactory interface [Media Foundation],described, mf.imfcaptureengineclassfactory, mfcaptureengine/IMFCaptureEngineClassFactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IMFCaptureEngineClassFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureEngineClassFactory interface


## -description


Creates an instance of the capture engine.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCaptureEngineClassFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFCaptureEngineClassFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFCaptureEngineClassFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D5E7D96B-9438-4332-AD05-249D2DA2481A">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates an instance of the capture engine.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call the <a href="https://msdn.microsoft.com/96f19dfb-a328-41db-8fa8-77f052b1a192">CoCreateInstance</a> function and specify the CLSID equal to <b>CLSID_MFCaptureEngineClassFactory</b>. 

Calling the <a href="https://msdn.microsoft.com/4B0C9DD6-135D-4412-A585-7E98A84101B5">MFCreateCaptureEngine</a> function is equivalent to calling <a href="https://msdn.microsoft.com/D5E7D96B-9438-4332-AD05-249D2DA2481A">IMFCaptureEngineClassFactory::CreateInstance</a>.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 


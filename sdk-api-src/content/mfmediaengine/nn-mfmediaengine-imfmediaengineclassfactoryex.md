---
UID: NN:mfmediaengine.IMFMediaEngineClassFactoryEx
title: IMFMediaEngineClassFactoryEx
author: windows-sdk-content
description: Extension for the IMFMediaEngineClassFactory interface.
old-location: mf\imfmediaengineclassfactoryex.htm
old-project: medfound
ms.assetid: d672ee59-f702-49c7-8ccf-5ba0260c9b23
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFMediaEngineClassFactoryEx, IMFMediaEngineClassFactoryEx interface [Media Foundation], IMFMediaEngineClassFactoryEx interface [Media Foundation],described, mf.imfmediaengineclassfactoryex, mfmediaengine/IMFMediaEngineClassFactoryEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngineClassFactoryEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineClassFactoryEx interface


## -description


Extension for the <a href="https://msdn.microsoft.com/8E4E84A0-BCFC-4CBF-813B-4FEE2B42A83E">IMFMediaEngineClassFactory</a> interface.


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
<a href="https://msdn.microsoft.com/40b2b978-f12c-4066-acf5-e0c68b0fa928">CreateMediaKeys</a>
</td>
<td align="left" width="63%">
Creates a media keys object based on the specified key system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a76bae3-0b7e-49fe-ab5d-bfb32d029d60">CreateMediaSourceExtension</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://msdn.microsoft.com/2acabcc2-242d-4b3d-b5b4-680c7973201f">IMFMediaSourceExtension</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f4f50db-e491-46c2-a8b2-1b8e51033b5b">IsTypeSupported</a>
</td>
<td align="left" width="63%">
Gets a value that indicates if the specified key system supports the specified media type.

</td>
</tr>
</table> 


## -remarks



This class is implemented by the Media Engine (CLSID_MFMediaEngineClassFactory).




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 


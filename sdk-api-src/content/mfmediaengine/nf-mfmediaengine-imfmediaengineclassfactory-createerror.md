---
UID: NF:mfmediaengine.IMFMediaEngineClassFactory.CreateError
title: IMFMediaEngineClassFactory::CreateError
author: windows-driver-content
description: Creates a media error object.
old-location: mf\imfmediaengineclassfactory_createerror.htm
old-project: medfound
ms.assetid: C089473D-CD35-4F5D-8C78-EDE0FA8C13EB
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: CreateError, CreateError method [Media Foundation], CreateError method [Media Foundation],IMFMediaEngineClassFactory interface, IMFMediaEngineClassFactory interface [Media Foundation],CreateError method, IMFMediaEngineClassFactory.CreateError, IMFMediaEngineClassFactory::CreateError, mf.imfmediaengineclassfactory_createerror, mfmediaengine/IMFMediaEngineClassFactory::CreateError
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngineClassFactory.CreateError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineClassFactory::CreateError


## -description


Creates a media error object.


## -parameters




### -param ppError [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/08F161FE-C0E5-44EE-923E-646ADA534C42">IMFMediaError</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8E4E84A0-BCFC-4CBF-813B-4FEE2B42A83E">IMFMediaEngineClassFactory</a>
 

 


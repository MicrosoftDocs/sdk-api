---
UID: NF:mfmediaengine.IMFMediaEngineExtension.EndCreateObject
title: IMFMediaEngineExtension::EndCreateObject
author: windows-sdk-content
description: Completes an asynchronous request to create a byte stream or media source.
old-location: mf\imfmediaengineextension_endcreateobject.htm
old-project: medfound
ms.assetid: F2B19870-7529-4C8C-9FE6-B312F6A2D2ED
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: EndCreateObject, EndCreateObject method [Media Foundation], EndCreateObject method [Media Foundation],IMFMediaEngineExtension interface, IMFMediaEngineExtension interface [Media Foundation],EndCreateObject method, IMFMediaEngineExtension.EndCreateObject, IMFMediaEngineExtension::EndCreateObject, mf.imfmediaengineextension_endcreateobject, mfmediaengine/IMFMediaEngineExtension::EndCreateObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MF_MEDIA_ENGINE_KEYERR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineExtension.EndCreateObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineExtension::EndCreateObject


## -description


Completes an asynchronous request to create a byte stream or media source.


## -parameters




### -param pResult [in]

A pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface.


### -param ppObject [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the byte stream or media source. The caller must release the interface


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Media Engine calls this method to complete the <a href="https://msdn.microsoft.com/804E9F16-E4C9-41F6-8913-950A569FB835">IMFMediaEngineExtension::BeginCreateObject</a> method.




## -see-also




<a href="https://msdn.microsoft.com/A032E0D0-2201-4B81-9FE0-8E9CE2707FDB">IMFMediaEngineExtension</a>
 

 


---
UID: NF:mfsharingengine.IMFSharingEngineClassFactory.CreateInstance
title: IMFSharingEngineClassFactory::CreateInstance
author: windows-sdk-content
description: Creates an instance of the media sharing engine.
old-location: mf\imfsharingengineclassfactory_createinstance.htm
tech.root: medfound
ms.assetid: 8410FA9C-22C1-412D-90ED-55F19F21B8BD
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CreateInstance, CreateInstance method [Media Foundation], CreateInstance method [Media Foundation],IMFSharingEngineClassFactory interface, IMFSharingEngineClassFactory interface [Media Foundation],CreateInstance method, IMFSharingEngineClassFactory.CreateInstance, IMFSharingEngineClassFactory::CreateInstance, mf.imfsharingengineclassfactory_createinstance, mfsharingengine/IMFSharingEngineClassFactory::CreateInstance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfsharingengine.h
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
 - mfsharingengine.h
api_name:
 - IMFSharingEngineClassFactory.CreateInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSharingEngineClassFactory::CreateInstance


## -description


Creates an instance of the media sharing engine.


## -parameters




### -param dwFlags [in]

A bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/1709B08C-D4DC-4A33-9B92-1C4961208684">MF_MEDIA_ENGINE_CREATEFLAGS</a> enumeration.


### -param pAttr [in]

A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. This parameter  specifies configuration attributes; see <a href="https://msdn.microsoft.com/08282D80-53F5-463F-B87F-522F72823E99">Media Engine Attributes</a>.


### -param ppEngine [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the media sharing engine. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/191CB50C-8CBB-470F-B558-F3A9EE554DA3">IMFSharingEngineClassFactory</a>
 

 


---
UID: NF:mfsharingengine.IPlayToSourceClassFactory.CreateInstance
title: IPlayToSourceClassFactory::CreateInstance (mfsharingengine.h)
author: windows-sdk-content
description: Creates an instance of the PlayToController object.
old-location: mf\iplaytosourceclassfactory_createinstance.htm
tech.root: medfound
ms.assetid: 3F7F8441-B0A2-407E-B127-C7DC66CA34DE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [Media Foundation], CreateInstance method [Media Foundation],IPlayToSourceClassFactory interface, IPlayToSourceClassFactory interface [Media Foundation],CreateInstance method, IPlayToSourceClassFactory.CreateInstance, IPlayToSourceClassFactory::CreateInstance, mf.iplaytocontrollerclassfactory_createinstance, mf.iplaytosourceclassfactory_createinstance, mfsharingengine/IPlayToSourceClassFactory::CreateInstance
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
 - IPlayToSourceClassFactory.CreateInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPlayToSourceClassFactory::CreateInstance


## -description


Creates an instance of the <b>PlayToController</b> object.


## -parameters




### -param dwFlags [in]

A bitwise <b>OR</b> of flags from the <a href="https://msdn.microsoft.com/15B632DD-586B-40E4-9B63-05CCC6AFB93A">PLAYTO_SOURCE_CREATEFLAGS</a> enumeration.


### -param pControl [in]

A pointer to the <a href="https://msdn.microsoft.com/53355EEA-559B-4803-89F6-D454E15F9254">IPlayToControl</a> interface.


### -param ppSource [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/F8F9FEC6-836C-429A-BADD-5CD1E550AED0">IPlayToSourceClassFactory</a>
 

 


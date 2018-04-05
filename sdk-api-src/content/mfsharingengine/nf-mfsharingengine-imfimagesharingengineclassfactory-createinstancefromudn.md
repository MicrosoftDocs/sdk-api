---
UID: NF:mfsharingengine.IMFImageSharingEngineClassFactory.CreateInstanceFromUDN
title: IMFImageSharingEngineClassFactory::CreateInstanceFromUDN method
author: windows-driver-content
description: Creates an instance of the IMFImageSharingEngine from the provided unique device name.
old-location: mf\imfimagesharingengineclassfactory_createinstancefromudn.htm
old-project: medfound
ms.assetid: 343E9CB5-12CA-4AC9-857F-D8324D035F07
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: CreateInstanceFromUDN method [Media Foundation], CreateInstanceFromUDN method [Media Foundation], IMFImageSharingEngineClassFactory interface, CreateInstanceFromUDN,IMFImageSharingEngineClassFactory.CreateInstanceFromUDN, IMFImageSharingEngineClassFactory, IMFImageSharingEngineClassFactory interface [Media Foundation], CreateInstanceFromUDN method, IMFImageSharingEngineClassFactory::CreateInstanceFromUDN, mf.imfimagesharingengineclassfactory_createinstancefromudn, mfsharingengine/IMFImageSharingEngineClassFactory::CreateInstanceFromUDN
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
req.typenames: PLAYTO_SOURCE_CREATEFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfsharingengine.h
api_name:
-	IMFImageSharingEngineClassFactory.CreateInstanceFromUDN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFImageSharingEngineClassFactory::CreateInstanceFromUDN method


## -description


Creates an instance of the <a href="https://msdn.microsoft.com/A30C73DA-9BD5-4D12-A6FB-771BBD2D1191">IMFImageSharingEngine</a> from the provided unique device name.


## -parameters




### -param pUniqueDeviceName

The unique device name of the device with which the sharing engine is created.


### -param ppEngine [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/A30C73DA-9BD5-4D12-A6FB-771BBD2D1191">IMFImageSharingEngine</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7D6385BC-4D9C-4026-9363-0F6917A62BDE">IMFImageSharingEngineClassFactory</a>
 

 


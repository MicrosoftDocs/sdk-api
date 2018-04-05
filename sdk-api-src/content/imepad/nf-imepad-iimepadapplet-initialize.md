---
UID: NF:imepad.IImePadApplet.Initialize
title: IImePadApplet::Initialize method
author: windows-driver-content
description: Called from IImePad interface to initialize IImePadApplet.
old-location: intl\iimepadapplet_initialize.htm
old-project: Intl
ms.assetid: E76FF3FC-717F-42B8-AC5E-45D5527882A7
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IImePadApplet, IImePadApplet interface [Internationalization for Windows Applications], Initialize method, IImePadApplet::Initialize, Initialize method [Internationalization for Windows Applications], Initialize method [Internationalization for Windows Applications], IImePadApplet interface, Initialize,IImePadApplet.Initialize, imepad/IImePadApplet::Initialize, intl.iimepadapplet_initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imepad.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PlatformId
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Imepad.h
api_name:
-	IImePadApplet.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IImePadApplet::Initialize method


## -description


Called from <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> interface to initialize <a href="https://msdn.microsoft.com/F3BC7176-9659-47B6-AFCA-049807394961">IImePadApplet</a>.


## -parameters




### -param lpIImePad

Pointer to <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> (<b>IUnknown</b> *)


## -returns



<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.




## -remarks



When the ImePad user interface is created, <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> calls this method and sets the IImePad interface pointer as an argument. The applet can save and use this pointer to call the <a href="https://msdn.microsoft.com/C74B0374-D6C7-44C7-94EF-E97B46534462">pIImePad->IImePad::Request</a> method.




## -see-also




<a href="https://msdn.microsoft.com/F3BC7176-9659-47B6-AFCA-049807394961">IImePadApplet</a>
 

 


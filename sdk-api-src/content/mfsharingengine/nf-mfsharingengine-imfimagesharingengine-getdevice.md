---
UID: NF:mfsharingengine.IMFImageSharingEngine.GetDevice
title: IMFImageSharingEngine::GetDevice
author: windows-driver-content
description: Gets information about the image sharing device.
old-location: mf\imfimagesharingengine_getdevice.htm
old-project: medfound
ms.assetid: 27CAE784-2107-4380-97E4-AE0A7D69C64F
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetDevice, GetDevice method [Media Foundation], GetDevice method [Media Foundation],IMFImageSharingEngine interface, IMFImageSharingEngine interface [Media Foundation],GetDevice method, IMFImageSharingEngine.GetDevice, IMFImageSharingEngine::GetDevice, mf.imfimagesharingengine_getdevice, mfsharingengine/IMFImageSharingEngine::GetDevice
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
-	IMFImageSharingEngine.GetDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFImageSharingEngine::GetDevice


## -description


Gets information about the image sharing device.


## -parameters




### -param pDevice [out]

A pointer to a <a href="https://msdn.microsoft.com/B006298C-B733-4E76-BD31-A3D1DD4DC766">DEVICE_INFO</a> structure. The method fills in this structure with the device information.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The method allocates memory for the <b>BSTR</b> members of the <a href="https://msdn.microsoft.com/B006298C-B733-4E76-BD31-A3D1DD4DC766">DEVICE_INFO</a> structure. The caller must free the memory for each <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/A30C73DA-9BD5-4D12-A6FB-771BBD2D1191">IMFImageSharingEngine</a>
 

 


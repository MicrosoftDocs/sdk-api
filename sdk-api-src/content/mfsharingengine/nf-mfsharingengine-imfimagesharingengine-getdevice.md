---
UID: NF:mfsharingengine.IMFImageSharingEngine.GetDevice
title: IMFImageSharingEngine::GetDevice (mfsharingengine.h)

description: Gets information about the image sharing device.
old-location: mf\imfimagesharingengine_getdevice.htm
tech.root: medfound
ms.assetid: 27CAE784-2107-4380-97E4-AE0A7D69C64F

ms.date: 12/05/2018
ms.keywords: GetDevice, GetDevice method [Media Foundation], GetDevice method [Media Foundation],IMFImageSharingEngine interface, IMFImageSharingEngine interface [Media Foundation],GetDevice method, IMFImageSharingEngine.GetDevice, IMFImageSharingEngine::GetDevice, mf.imfimagesharingengine_getdevice, mfsharingengine/IMFImageSharingEngine::GetDevice
ms.topic: method
f1_keywords: 
 - "mfsharingengine/IMFImageSharingEngine.GetDevice"
dev_langs:
 - c++
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
 - IMFImageSharingEngine.GetDevice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFImageSharingEngine::GetDevice


## -description


Gets information about the image sharing device.


## -parameters




### -param pDevice [out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/mfsharingengine/ns-mfsharingengine-device_info">DEVICE_INFO</a> structure. The method fills in this structure with the device information.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The method allocates memory for the <b>BSTR</b> members of the <a href="https://docs.microsoft.com/windows/desktop/api/mfsharingengine/ns-mfsharingengine-device_info">DEVICE_INFO</a> structure. The caller must free the memory for each <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengine">IMFImageSharingEngine</a>
 

 


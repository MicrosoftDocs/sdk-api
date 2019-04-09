---
UID: NF:strmif.IAMExtDevice.get_ExternalDeviceVersion
title: IAMExtDevice::get_ExternalDeviceVersion (strmif.h)
author: windows-sdk-content
description: The get_ExternalDeviceVersion retrieves the version number of the external device's operating software.
old-location: dshow\iamextdevice_get_externaldeviceversion.htm
tech.root: DirectShow
ms.assetid: 66a98ad3-850a-4b41-a169-f971fde83266
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMExtDevice interface [DirectShow],get_ExternalDeviceVersion method, IAMExtDevice.get_ExternalDeviceVersion, IAMExtDevice::get_ExternalDeviceVersion, IAMExtDeviceget_ExternalDeviceVersion, dshow.iamextdevice_get_externaldeviceversion, get_ExternalDeviceVersion, get_ExternalDeviceVersion method [DirectShow], get_ExternalDeviceVersion method [DirectShow],IAMExtDevice interface, strmif/IAMExtDevice::get_ExternalDeviceVersion
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMExtDevice.get_ExternalDeviceVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMExtDevice::get_ExternalDeviceVersion


## -description



The <code>get_ExternalDeviceVersion</code> retrieves the version number of the external device's operating software.




## -parameters




### -param ppszData [out]

Pointer to an <b>LPOLESTR</b> that receives the manufacturer-specific operating software version number as a string. The caller must release the string by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0423e888-39d1-45cb-9bcf-722240a31fbd">IAMExtDevice Interface</a>
 

 


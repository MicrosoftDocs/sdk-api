---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetFormatRenderingProfiles
title: IPortableDeviceServiceCapabilities::GetFormatRenderingProfiles
author: windows-sdk-content
description: Retrieves the rendering profiles of a format.
old-location: wpdsdk\iportabledeviceservicecapabilities_getformatrenderingprofiles.htm
old-project: wpd_sdk
ms.assetid: 38c9d357-17aa-4b26-9c01-c13a5cfcf495
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: GetFormatRenderingProfiles, GetFormatRenderingProfiles method [Windows Portable Devices SDK], GetFormatRenderingProfiles method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetFormatRenderingProfiles method, IPortableDeviceServiceCapabilities.GetFormatRenderingProfiles, IPortableDeviceServiceCapabilities::GetFormatRenderingProfiles, portabledeviceapi/IPortableDeviceServiceCapabilities::GetFormatRenderingProfiles, wpdsdk.iportabledeviceservicecapabilities_getformatrenderingprofiles
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: PortableDeviceAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceServiceCapabilities.GetFormatRenderingProfiles
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPortableDeviceServiceCapabilities::GetFormatRenderingProfiles


## -description


The <b>GetFormatRenderingProfiles</b> method retrieves the rendering profiles of a format.


## -parameters




### -param Format [in]

The format whose rendering profiles are retrieved.


### -param ppRenderingProfiles [out]

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597598">IPortableDeviceValuesCollection</a> object that receives the list of rendering profiles.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



The rendering profiles are similar to what the <a href="https://msdn.microsoft.com/library/windows/hardware/ff597881">WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION</a> functional object returns for device-wide rendering profiles, so that the <b>DisplayRenderingProfile</b> helper function described in <a href="https://msdn.microsoft.com/2332e3cc-087c-49cf-bde9-7f86f65158e7">Retrieving the Rendering Capabilities Supported by a Device</a> could be used here as well.    But there are differences: The <b>GetFormatRenderingProfiles</b> method retrieves only rendering profiles that apply to the selected service and have been filtered by format.




## -see-also




<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>
 

 


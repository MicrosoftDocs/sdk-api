---
UID: NF:vdshwprv.IVdsProviderSupport.GetVersionSupport
title: IVdsProviderSupport::GetVersionSupport
author: windows-sdk-content
description: Returns a bitmask of values enumerated by VDS_VERSION_SUPPORT_FLAG indicating the versions of the VDS interfaces supported by this provider.
old-location: base\ivdsprovidersupport_getversionsupport.htm
tech.root: VDS
ms.assetid: c7527d29-7ab4-4f98-991b-411059e14237
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetVersionSupport, GetVersionSupport method, GetVersionSupport method,IVdsProviderSupport interface, IVdsProviderSupport interface,GetVersionSupport method, IVdsProviderSupport.GetVersionSupport, IVdsProviderSupport::GetVersionSupport, base.ivdsprovidersupport_getversionsupport, vds/IVdsProviderSupport::GetVersionSupport, vdshwprv/IVdsProviderSupport::GetVersionSupport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsProviderSupport.GetVersionSupport
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
---

# IVdsProviderSupport::GetVersionSupport


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns a bitmask of values enumerated by 
    <a href="https://msdn.microsoft.com/c145070f-587f-42d7-bde9-3bf0cdba8444">VDS_VERSION_SUPPORT_FLAG</a> indicating the versions 
    of the VDS interfaces supported by this provider. This method is implemented only by hardware providers.


## -parameters




### -param ulVersionSupport [out]

Address of a <b>ULONG</b> that receives a bitmask of one or more of the values enumerated by 
      <a href="https://msdn.microsoft.com/c145070f-587f-42d7-bde9-3bf0cdba8444">VDS_VERSION_SUPPORT_FLAG</a> indicating the 
      versions of the VDS interfaces supported by the provider.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used.




## -see-also




<a href="https://msdn.microsoft.com/74e17a86-75ec-429b-9efb-80812ca4b431">IVdsProviderSupport</a>



<a href="https://msdn.microsoft.com/c145070f-587f-42d7-bde9-3bf0cdba8444">VDS_VERSION_SUPPORT_FLAG</a>
 

 


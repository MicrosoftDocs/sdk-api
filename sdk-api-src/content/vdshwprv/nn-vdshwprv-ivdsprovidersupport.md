---
UID: NN:vdshwprv.IVdsProviderSupport
title: IVdsProviderSupport (vdshwprv.h)
author: windows-sdk-content
description: Provides a method to indicate what versions of the VDS interfaces are supported by the provider.
old-location: base\ivdsprovidersupport.htm
tech.root: VDS
ms.assetid: 74e17a86-75ec-429b-9efb-80812ca4b431
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsProviderSupport, IVdsProviderSupport interface, IVdsProviderSupport interface,described, base.ivdsprovidersupport, vds/IVdsProviderSupport, vdshwprv/IVdsProviderSupport
ms.topic: interface
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
 - IVdsProviderSupport
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
---

# IVdsProviderSupport interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides a method 
    to indicate what versions of the VDS interfaces are supported by the provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsProviderSupport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsProviderSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsProviderSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7527d29-7ab4-4f98-991b-411059e14237">GetVersionSupport</a>
</td>
<td align="left" width="63%">
Returns a bitmask of values enumerated by 
     <a href="https://msdn.microsoft.com/c145070f-587f-42d7-bde9-3bf0cdba8444">VDS_VERSION_SUPPORT_FLAG</a> indicating the 
     versions of the VDS interfaces supported by this provider.</p> (Inherited from <b>IVdsProviderSupport</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 


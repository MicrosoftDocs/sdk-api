---
UID: NE:wmsdkidl.tagWMT_DRMLA_TRUST
title: tagWMT_DRMLA_TRUST
author: windows-sdk-content
description: Defines the trust state of a DRM license acquisition URL.
old-location: wmformat\wmt_drmla_trust.htm
tech.root: wmformat
ms.assetid: 48c62532-1cb5-4073-8fa9-cab5a8355bc3
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: WMT_DRMLA_TAMPERED, WMT_DRMLA_TRUST, WMT_DRMLA_TRUST enumeration [windows Media Format], WMT_DRMLA_TRUSTED, WMT_DRMLA_UNTRUSTED, tagWMT_DRMLA_TRUST, wmformat.wmt_drmla_trust, wmsdkidl/WMT_DRMLA_TAMPERED, wmsdkidl/WMT_DRMLA_TRUST, wmsdkidl/WMT_DRMLA_TRUSTED, wmsdkidl/WMT_DRMLA_UNTRUSTED
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_DRMLA_TRUST
product: Windows
targetos: Windows
req.typenames: WMT_DRMLA_TRUST
req.redist: 
---

# tagWMT_DRMLA_TRUST enumeration


## -description



Defines the trust state of a DRM license acquisition URL.




## -enum-fields




### -field WMT_DRMLA_UNTRUSTED

Indicates that the validity of the license acquisition URL cannot be guaranteed because it is not signed. All protected content created prior to Windows Media 9 Series will cause this value to be returned.


### -field WMT_DRMLA_TRUSTED

Indicates that the license acquisition URL is the original one provided with the content.


### -field WMT_DRMLA_TAMPERED

Indicates that the license acquisition URL was originally signed and has been tampered with.


## -remarks



When a <b>WMT_LICENSEURL_SIGNATURE_STATE</b> message is received in the <b>OnStatus</b> callback method, pValue will be set to one of the <b>WMT_DRMLA_TRUST</b> constants, which indicate whether there is any problem with the digital signature applied to the license acquisition URL.




## -see-also




<a href="https://msdn.microsoft.com/cd28f608-25ba-44a7-868b-b1cd4dfcfa45">Enumeration Types</a>
 

 


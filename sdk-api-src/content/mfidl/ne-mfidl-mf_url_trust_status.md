---
UID: NE:mfidl.__MIDL___MIDL_itf_mfidl_0000_0032_0001
title: MF_URL_TRUST_STATUS (mfidl.h)
description: Indicates whether the URL is from a trusted source.
helpviewer_keywords: ["MF_LICENSE_URL_TAMPERED","MF_LICENSE_URL_TRUSTED","MF_LICENSE_URL_UNTRUSTED","MF_URL_TRUST_STATUS","MF_URL_TRUST_STATUS enumeration [Media Foundation]","fd008a23-71f7-4718-a51a-ee88453b6fdd","mf.mf_url_trust_status","mfidl/MF_LICENSE_URL_TAMPERED","mfidl/MF_LICENSE_URL_TRUSTED","mfidl/MF_LICENSE_URL_UNTRUSTED","mfidl/MF_URL_TRUST_STATUS"]
old-location: mf\mf_url_trust_status.htm
tech.root: mf
ms.assetid: fd008a23-71f7-4718-a51a-ee88453b6fdd
ms.date: 12/05/2018
ms.keywords: MF_LICENSE_URL_TAMPERED, MF_LICENSE_URL_TRUSTED, MF_LICENSE_URL_UNTRUSTED, MF_URL_TRUST_STATUS, MF_URL_TRUST_STATUS enumeration [Media Foundation], fd008a23-71f7-4718-a51a-ee88453b6fdd, mf.mf_url_trust_status, mfidl/MF_LICENSE_URL_TAMPERED, mfidl/MF_LICENSE_URL_TRUSTED, mfidl/MF_LICENSE_URL_UNTRUSTED, mfidl/MF_URL_TRUST_STATUS
f1_keywords:
- mfidl/MF_URL_TRUST_STATUS
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
- mfidl.h
api_name:
- MF_URL_TRUST_STATUS
targetos: Windows
req.typenames: MF_URL_TRUST_STATUS
req.redist: 
ms.custom: 19H1
---

# MF_URL_TRUST_STATUS enumeration


## -description



Indicates whether the URL is from a trusted source.




## -enum-fields




### -field MF_LICENSE_URL_UNTRUSTED:0

The validity of the URL cannot be guaranteed because it is not signed. The application should warn the user.


### -field MF_LICENSE_URL_TRUSTED

The URL is the original one provided with the content.


### -field MF_LICENSE_URL_TAMPERED

The URL was originally signed and has been tampered with. The file should be considered corrupted, and the application should not navigate to the URL without issuing a strong warning the user.


## -see-also




<a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl">IMFContentEnabler::GetEnableURL</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
 

 

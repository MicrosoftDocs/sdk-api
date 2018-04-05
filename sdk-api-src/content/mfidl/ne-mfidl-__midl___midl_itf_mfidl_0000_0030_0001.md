---
UID: NE:mfidl.__MIDL___MIDL_itf_mfidl_0000_0030_0001
title: "__MIDL___MIDL_itf_mfidl_0000_0030_0001"
author: windows-driver-content
description: Indicates whether the URL is from a trusted source.
old-location: mf\mf_url_trust_status.htm
old-project: medfound
ms.assetid: fd008a23-71f7-4718-a51a-ee88453b6fdd
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: MF_LICENSE_URL_TAMPERED, MF_LICENSE_URL_TRUSTED, MF_LICENSE_URL_UNTRUSTED, MF_URL_TRUST_STATUS, MF_URL_TRUST_STATUS enumeration [Media Foundation], __MIDL___MIDL_itf_mfidl_0000_0030_0001, fd008a23-71f7-4718-a51a-ee88453b6fdd, mf.mf_url_trust_status, mfidl/MF_LICENSE_URL_TAMPERED, mfidl/MF_LICENSE_URL_TRUSTED, mfidl/MF_LICENSE_URL_UNTRUSTED, mfidl/MF_URL_TRUST_STATUS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfidl.h
api_name:
-	MF_URL_TRUST_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_mfidl_0000_0030_0001 enumeration


## -description



Indicates whether the URL is from a trusted source.




## -enum-fields




### -field MF_LICENSE_URL_UNTRUSTED

The validity of the URL cannot be guaranteed because it is not signed. The application should warn the user.


### -field MF_LICENSE_URL_TRUSTED

The URL is the original one provided with the content.


### -field MF_LICENSE_URL_TAMPERED

The URL was originally signed and has been tampered with. The file should be considered corrupted, and the application should not navigate to the URL without issuing a strong warning the user.


## -see-also




<a href="https://msdn.microsoft.com/1a44216d-36e5-4b5c-9585-5297d5e429f9">IMFContentEnabler::GetEnableURL</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 


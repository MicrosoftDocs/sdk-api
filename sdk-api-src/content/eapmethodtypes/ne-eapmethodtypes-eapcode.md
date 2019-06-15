---
UID: NE:eapmethodtypes.tagEapCode
title: EapCode (eapmethodtypes.h)
author: windows-sdk-content
description: Defines the set of EAP packet types.
old-location: eaphost\eapcode.htm
tech.root: eaphost
ms.assetid: 19d424a1-91d6-4ebd-acb8-912b4900a4cd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapCode, EapCode enumeration [EAPHost], EapCodeFailure, EapCodeMaximum, EapCodeMinimum, EapCodeRequest, EapCodeResponse, EapCodeSuccess, eaphost.eapcode, eapmethodtypes/EapCode, eapmethodtypes/EapCodeFailure, eapmethodtypes/EapCodeMaximum, eapmethodtypes/EapCodeMinimum, eapmethodtypes/EapCodeRequest, eapmethodtypes/EapCodeResponse, eapmethodtypes/EapCodeSuccess
ms.topic: enum
req.header: eapmethodtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - eapmethodtypes.h
api_name:
 - EapCode
product: Windows
targetos: Windows
req.typenames: EapCode
req.redist: 
ms.custom: 19H1
---

# EapCode enumeration


## -description


 The <b>EapCode</b> enumeration defines the set of EAP packet types.


## -enum-fields




### -field EapCodeMinimum

The lowest possible value for an EAP packet type code. 


### -field EapCodeRequest

A request packet sent by the authenticator to the supplicant.


### -field EapCodeResponse

A response packet sent by the supplicant to the authenticator.


### -field EapCodeSuccess

A successful authentication attempt.


### -field EapCodeFailure

A failed authentication attempt.


### -field EapCodeMaximum

The highest possible value for an EAP packet type code.


### -field v1_enum




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodtypes/ns-eapmethodtypes-tageappacket">EapPacket</a>
 

 


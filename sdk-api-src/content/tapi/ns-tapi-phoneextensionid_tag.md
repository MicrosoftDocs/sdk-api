---
UID: NS:tapi.phoneextensionid_tag
title: phoneextensionid_tag
author: windows-sdk-content
description: The PHONEEXTENSIONID structure describes an extension identifier.
old-location: tapi2\phoneextensionid_str.htm
tech.root: tapi
ms.assetid: 61f376fd-2287-4425-9445-163f71aebf04
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*LPPHONEEXTENSIONID, LPPHONEEXTENSIONID, LPPHONEEXTENSIONID structure pointer [TAPI 2.2], PHONEEXTENSIONID, PHONEEXTENSIONID structure [TAPI 2.2], _tapi2_phoneextensionid_str, phoneextensionid_tag, tapi/LPPHONEEXTENSIONID, tapi/PHONEEXTENSIONID, tapi2.phoneextensionid_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - Tapi.h
api_name:
 - PHONEEXTENSIONID
product: Windows
targetos: Windows
req.typenames: PHONEEXTENSIONID, *LPPHONEEXTENSIONID
req.redist: 
---

# phoneextensionid_tag structure


## -description


The 
<b>PHONEEXTENSIONID</b> structure describes an extension identifier. Extension identifiers are used to identify service provider-specific extensions for phone device classes. The 
<a href="https://msdn.microsoft.com/50c2c15c-459f-451b-9b79-9118acc81c8c">phoneNegotiateAPIVersion</a> and 
<a href="https://msdn.microsoft.com/c4c1c68f-0a48-40f2-8eb9-f54c3572578c">TSPI_phoneGetExtensionID</a> functions return this structure.


## -struct-fields




### -field dwExtensionID0

First part of the extension identifier.


### -field dwExtensionID1

Second part of the extension identifier.


### -field dwExtensionID2

Third part of the extension identifier.


### -field dwExtensionID3

Fourth part of the extension identifier.


## -remarks



These four members together specify a universally unique extension identifier that identifies a phone device class extension. This structure may not be extended.

Extension identifiers are generated using an SDK-provided generation utility.




## -see-also




<a href="https://msdn.microsoft.com/c4c1c68f-0a48-40f2-8eb9-f54c3572578c">TSPI_phoneGetExtensionID</a>



<a href="https://msdn.microsoft.com/50c2c15c-459f-451b-9b79-9118acc81c8c">phoneNegotiateAPIVersion</a>
 

 


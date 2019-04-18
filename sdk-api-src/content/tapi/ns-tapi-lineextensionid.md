---
UID: NS:tapi.lineextensionid_tag
title: LINEEXTENSIONID (tapi.h)
author: windows-sdk-content
description: The LINEEXTENSIONID structure describes an extension identifier.
old-location: tapi2\lineextensionid_str.htm
tech.root: Tapi
ms.assetid: bf7d9ccc-3f80-4e54-bcc2-cc2fef1d24af
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPLINEEXTENSIONID, LINEEXTENSIONID, LINEEXTENSIONID structure [TAPI 2.2], LPLINEEXTENSIONID, LPLINEEXTENSIONID structure pointer [TAPI 2.2], _tapi2_lineextensionid_str, tapi/LINEEXTENSIONID, tapi/LPLINEEXTENSIONID, tapi2.lineextensionid_str"
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
 - LINEEXTENSIONID
product: Windows
targetos: Windows
req.typenames: LINEEXTENSIONID, *LPLINEEXTENSIONID
req.redist: 
ms.custom: 19H1
---

# LINEEXTENSIONID structure


## -description


The 
<b>LINEEXTENSIONID</b> structure describes an extension identifier. Extension identifiers are used to identify service provider-specific extensions for line devices. Multiple functions use this structure, including the 
<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a> function and the 
<a href="https://msdn.microsoft.com/aaea0a6a-bf22-491f-b1bf-d2195fba6af5">TSPI_lineGetExtensionID</a> function.


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



These four members together specify a universally unique extension identifier that identifies a line device class extension. This structure may not be extended.

Extension identifiers are generated using an SDK-provided generation utility.




## -see-also




<a href="https://msdn.microsoft.com/aaea0a6a-bf22-491f-b1bf-d2195fba6af5">TSPI_lineGetExtensionID</a>



<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a>
 

 


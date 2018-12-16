---
UID: NF:webservices.WS_XML_STRING_VALUE
title: WS_XML_STRING_VALUE macro
author: windows-sdk-content
description: Provides an initializer for a WS_XML_STRING structure when there is no associated dictionary ID.
old-location: wsw\ws_xml_string_value.htm
tech.root: wsw
ms.assetid: 95e2326c-d4b2-421c-b991-ca9c332b6f6f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_XML_STRING_VALUE, WS_XML_STRING_VALUE macro [Web Services for Windows], webservices/WS_XML_STRING_VALUE, wsw.ws_xml_string_value
ms.topic: macro
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - WebServices.h
api_name:
 - WS_XML_STRING_VALUE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WS_XML_STRING_VALUE macro


## -description


Provides an initializer for a <a href="https://msdn.microsoft.com/3daa656f-7f97-4e29-a556-7ff72206f01c">WS_XML_STRING</a> structure when there is no associated dictionary ID.
      


## -parameters




### -param S

TBD






## -remarks



This initializer assumes the string is a static constant string.  It must be encoded in UTF-8.
      

The following is example usage:
      

<code>WS_XML_STRING myString = WS_XML_STRING_VALUE("MyString");</code>




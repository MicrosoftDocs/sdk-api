---
UID: NS:webservices._WS_XML_QNAME_DESCRIPTION
title: "_WS_XML_QNAME_DESCRIPTION"
author: windows-sdk-content
description: This type description is used with WS_XML_QNAME_TYPE and is optional. It is used to specify constraints on the set of values which can be deserialized.
old-location: wsw\ws_xml_qname_description.htm
old-project: wsw
ms.assetid: 300c5fd1-1a66-40b8-9f26-0f0711f7a527
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WS_XML_QNAME_DESCRIPTION, WS_XML_QNAME_DESCRIPTION structure [Web Services for Windows], _WS_XML_QNAME_DESCRIPTION, webservices/WS_XML_QNAME_DESCRIPTION, wsw.ws_xml_qname_description
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WS_XML_QNAME_DESCRIPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_XML_QNAME_DESCRIPTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_XML_QNAME_DESCRIPTION structure


## -description


This type description is used with <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_XML_QNAME_TYPE</a> and is optional.
                It is used to specify constraints on the set of values
                which can be deserialized.
            


## -struct-fields




### -field minLocalNameByteCount

The minimum number of bytes of UTF8 character data 
                    for the local name string.
                


### -field maxLocalNameByteCount

The maximum number of bytes of UTF8 character data
                    for the local name string.
                


### -field minNsByteCount

The minimum number of bytes of UTF8 character data 
                    for the namespace string.
                


### -field maxNsByteCount

The maximum number of bytes of UTF8 character data 
                    for the namespace string.
                


---
UID: NE:webservices.__unnamed_enum_12
title: "__unnamed_enum_12"
author: windows-sdk-content
description: Flags that control behavior of WsDecodeUrl, WsEncodeUrl, and WsCombineUrl.
old-location: wsw\ws_url_flags.htm
tech.root: wsw
ms.assetid: b74c22fd-35b1-4d7b-974d-8ff7fff07813
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WS_URL_FLAGS, WS_URL_FLAGS enumeration [Web Services for Windows], WS_URL_FLAGS_ALLOW_HOST_WILDCARDS, WS_URL_FLAGS_NO_PATH_COLLAPSE, WS_URL_FLAGS_ZERO_TERMINATE, __unnamed_enum_12, webservices/WS_URL_FLAGS, webservices/WS_URL_FLAGS_ALLOW_HOST_WILDCARDS, webservices/WS_URL_FLAGS_NO_PATH_COLLAPSE, webservices/WS_URL_FLAGS_ZERO_TERMINATE, wsw.ws_url_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - WS_URL_FLAGS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# __unnamed_enum_12 enumeration


## -description


Flags that control behavior of <a href="https://msdn.microsoft.com/67147b71-ca3a-4a17-a4f1-6ba608eca742">WsDecodeUrl</a>, <a href="https://msdn.microsoft.com/8253b062-072b-4d37-8b82-407df1bea6b4">WsEncodeUrl</a>,
                and <a href="https://msdn.microsoft.com/6cff906a-adb7-4453-8d44-6a5bf44a681b">WsCombineUrl</a>.
            


## -enum-fields




### -field WS_URL_FLAGS_ALLOW_HOST_WILDCARDS

The wild cards '*' and '+' should be accepted for the hostname.
                    This flag applies to <a href="https://msdn.microsoft.com/67147b71-ca3a-4a17-a4f1-6ba608eca742">WsDecodeUrl</a> and <a href="https://msdn.microsoft.com/6cff906a-adb7-4453-8d44-6a5bf44a681b">WsCombineUrl</a> only.
                


### -field WS_URL_FLAGS_NO_PATH_COLLAPSE

By default path segments '.' are deleted, and path segments '..' removes the immediately preceding
                    path segment.  If WS_URL_FLAGS_NO_PATH_COLLAPSE is specified, then this behavior does not occur and
                    path segments containing '.' and '..' are returned unaltered.
                    This flag applies to <a href="https://msdn.microsoft.com/67147b71-ca3a-4a17-a4f1-6ba608eca742">WsDecodeUrl</a> and <a href="https://msdn.microsoft.com/6cff906a-adb7-4453-8d44-6a5bf44a681b">WsCombineUrl</a>only.
                


### -field WS_URL_FLAGS_ZERO_TERMINATE

By default the string returned from <a href="https://msdn.microsoft.com/8253b062-072b-4d37-8b82-407df1bea6b4">WsEncodeUrl</a> is not guaranteed to be zero terminated.
                    If WS_URL_FLAGS_ZERO_TERMINATE is specified, then <b>WsEncodeUrl</b> will return zero terminated string.
                    The length will include the zero terminator character.
                    This flag applies to <b>WsEncodeUrl</b> and <a href="https://msdn.microsoft.com/6cff906a-adb7-4453-8d44-6a5bf44a681b">WsCombineUrl</a>only.
                


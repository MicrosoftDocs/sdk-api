---
UID: NS:appxpackaging.APPX_PACKAGE_WRITER_PAYLOAD_STREAM
title: APPX_PACKAGE_WRITER_PAYLOAD_STREAM (appxpackaging.h)
author: windows-sdk-content
description: Contains the data and metadata of files to write into the app package.
old-location: appxpkg\appx_package_writer_payload_stream.htm
tech.root: appxpkg
ms.assetid: 0AB54C4B-6982-49A3-BFD3-E46E75954B08
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: APPX_PACKAGE_WRITER_PAYLOAD_STREAM, APPX_PACKAGE_WRITER_PAYLOAD_STREAM structure [App packaging and management], appxpackaging/APPX_PACKAGE_WRITER_PAYLOAD_STREAM, appxpkg.appx_package_writer_payload_stream
ms.topic: struct
f1_keywords: 
 - "appxpackaging/APPX_PACKAGE_WRITER_PAYLOAD_STREAM"
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
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
 - AppxPackaging.h
api_name:
 - APPX_PACKAGE_WRITER_PAYLOAD_STREAM
product: Windows
targetos: Windows
req.typenames: APPX_PACKAGE_WRITER_PAYLOAD_STREAM
req.redist: 
ms.custom: 19H1
---

# APPX_PACKAGE_WRITER_PAYLOAD_STREAM structure


## -description


Contains the data and metadata of files to write into the app package.


## -struct-fields




### -field inputStream

The source of the payload file.


### -field fileName

Name of the payload file.


### -field contentType

The content type of the payload file.


### -field compressionOption

 The degree of compression used for the file in the package.


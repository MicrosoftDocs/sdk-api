---
UID: NE:appxpackaging.APPX_COMPRESSION_OPTION
title: APPX_COMPRESSION_OPTION
author: windows-driver-content
description: Specifies the degree of compression used to store the file in the package.
old-location: appxpkg\appx_compression_option.htm
old-project: appxpkg
ms.assetid: C4FEE4DA-1097-4870-BB43-A910E20BCBD6
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: APPX_COMPRESSION_OPTION, APPX_COMPRESSION_OPTION enumeration [App packaging and management], APPX_COMPRESSION_OPTION_FAST, APPX_COMPRESSION_OPTION_MAXIMUM, APPX_COMPRESSION_OPTION_NONE, APPX_COMPRESSION_OPTION_NORMAL, APPX_COMPRESSION_OPTION_SUPERFAST, appxpackaging/APPX_COMPRESSION_OPTION, appxpackaging/APPX_COMPRESSION_OPTION_FAST, appxpackaging/APPX_COMPRESSION_OPTION_MAXIMUM, appxpackaging/APPX_COMPRESSION_OPTION_NONE, appxpackaging/APPX_COMPRESSION_OPTION_NORMAL, appxpackaging/APPX_COMPRESSION_OPTION_SUPERFAST, appxpkg.appx_compression_option
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: APPX_COMPRESSION_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	AppxPackaging.h
api_name:
-	APPX_COMPRESSION_OPTION
product: Windows
targetos: Windows
req.lib: Appnotify.lib
req.dll: Twinapi.core.dll
req.irql: 
---

# APPX_COMPRESSION_OPTION enumeration


## -description


Specifies the degree of compression used to store the file in the package.


## -enum-fields




### -field APPX_COMPRESSION_OPTION_NONE

No compression.


### -field APPX_COMPRESSION_OPTION_NORMAL

Normal  compression.


### -field APPX_COMPRESSION_OPTION_MAXIMUM

Maximum compression.


### -field APPX_COMPRESSION_OPTION_FAST

Fast compression.


### -field APPX_COMPRESSION_OPTION_SUPERFAST

Super-fast compression.


## -see-also




<a href="https://msdn.microsoft.com/E2F33ED4-EAD3-44AE-B646-3AB875FA7606">IAppxFile::GetCompressionOption</a>



<a href="https://msdn.microsoft.com/2BFC725A-CD56-46CA-983A-FD1BFB6CB474">IAppxPackageWriter::AddPayloadFile</a>
 

 


---
UID: NE:appxpackaging.APPX_COMPRESSION_OPTION
title: APPX_COMPRESSION_OPTION (appxpackaging.h)
author: windows-sdk-content
description: Specifies the degree of compression used to store the file in the package.
old-location: appxpkg\appx_compression_option.htm
tech.root: appxpkg
ms.assetid: C4FEE4DA-1097-4870-BB43-A910E20BCBD6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: APPX_COMPRESSION_OPTION, APPX_COMPRESSION_OPTION enumeration [App packaging and management], APPX_COMPRESSION_OPTION_FAST, APPX_COMPRESSION_OPTION_MAXIMUM, APPX_COMPRESSION_OPTION_NONE, APPX_COMPRESSION_OPTION_NORMAL, APPX_COMPRESSION_OPTION_SUPERFAST, appxpackaging/APPX_COMPRESSION_OPTION, appxpackaging/APPX_COMPRESSION_OPTION_FAST, appxpackaging/APPX_COMPRESSION_OPTION_MAXIMUM, appxpackaging/APPX_COMPRESSION_OPTION_NONE, appxpackaging/APPX_COMPRESSION_OPTION_NORMAL, appxpackaging/APPX_COMPRESSION_OPTION_SUPERFAST, appxpkg.appx_compression_option
ms.topic: enum
f1_keywords: 
 - "appxpackaging/APPX_COMPRESSION_OPTION"
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
 - APPX_COMPRESSION_OPTION
targetos: Windows
req.typenames: APPX_COMPRESSION_OPTION
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfile-getcompressionoption">IAppxFile::GetCompressionOption</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagewriter-addpayloadfile">IAppxPackageWriter::AddPayloadFile</a>
 

 


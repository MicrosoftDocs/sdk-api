---
UID: NS:ndkinfo.NDK_VERSION
title: NDK_VERSION
author: windows-sdk-content
description: The NDK_VERSION structure specifies major and minor versions in the NDK interface.
old-location: netvista\ndk_version.htm
tech.root: netvista
ms.assetid: 10A5A3E6-7257-4560-8452-607EC7C54397
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: NDK_VERSION, NDK_VERSION structure [Network Drivers Starting with Windows Vista], ndkinfo/NDK_VERSION, netvista.ndk_version
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ndkinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported,Supported in NDIS 6.30 and later.
req.target-min-winversvr: Windows Server 2012
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
 - ndkinfo.h
api_name:
 - NDK_VERSION
product: Windows
targetos: Windows
req.typenames: NDK_VERSION
req.redist: 
---

# NDK_VERSION structure


## -description


The <b>NDK_VERSION</b> structure specifies major and minor versions in the NDK interface.


## -struct-fields




### -field Major

The NDK major version number.


### -field Minor

The NDK minor version number.


## -remarks



This structure is used to specify NDK version numbers in several NDK structures and functions.

To specify version 1.1 (for Windows Server 2012), set both the <b>Major</b> and <b>Minor</b> members to 1.

To specify version 1.2 (for Windows Server 2012 R2), set the <b>Major</b> member to 1 and the <b>Minor</b> member to 2.




## -see-also




<a href="https://msdn.microsoft.com/AC8D4FA1-59E0-4934-A6C5-EA2E645C53FA">NDIS_OPEN_NDK_ADAPTER_PARAMETERS</a>



<a href="https://msdn.microsoft.com/3F8EAA7F-20CE-4948-9F10-E23025B174E7">NDK_ADAPTER_INFO</a>



<a href="https://msdn.microsoft.com/439C990E-6978-4D0F-8453-6EB2FED1DB77">NDK_FN_QUERY_EXTENSION_INTERFACE</a>



<a href="https://msdn.microsoft.com/12E3ED4A-F078-4489-BC84-69EE735CAEF8">NDK_OBJECT_HEADER</a>
 

 


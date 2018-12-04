---
UID: NS:wincrypt._CERT_LOGOTYPE_DATA
title: "_CERT_LOGOTYPE_DATA"
author: windows-sdk-content
description: Contains logotype data.
old-location: security\cert_logotype_data.htm
tech.root: seccrypto
ms.assetid: f170dd48-a0f4-45e0-b5b8-a5f446d1a86e
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PCERT_LOGOTYPE_DATA, CERT_LOGOTYPE_DATA, CERT_LOGOTYPE_DATA structure [Security], PCERT_LOGOTYPE_DATA, PCERT_LOGOTYPE_DATA structure pointer [Security], _CERT_LOGOTYPE_DATA, security.cert_logotype_data, wincrypt/CERT_LOGOTYPE_DATA, wincrypt/PCERT_LOGOTYPE_DATA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincrypt.h
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
 - Wincrypt.h
api_name:
 - CERT_LOGOTYPE_DATA
product: Windows
targetos: Windows
req.typenames: CERT_LOGOTYPE_DATA, *PCERT_LOGOTYPE_DATA
req.redist: 
---

# _CERT_LOGOTYPE_DATA structure


## -description


The <b>CERT_LOGOTYPE_DATA</b> structure contains logotype data.


## -struct-fields




### -field cLogotypeImage

The number of elements in the <b>rgLogotypeImage</b> array.


### -field rgLogotypeImage

An array of <a href="https://msdn.microsoft.com/d1dff71c-41e1-4f02-93b4-019d688ed012">CERT_LOGOTYPE_IMAGE</a> structures that contain the logotype images. The <b>cLogotypeImage</b> member contains the number of elements in this array.


### -field cLogotypeAudio

The number of elements in the <b>rgLogotypeAudio</b> array.


### -field rgLogotypeAudio

An array of <a href="https://msdn.microsoft.com/97357faa-2720-4240-a3c3-77abdce8d86d">CERT_LOGOTYPE_AUDIO</a> structures that contain the logotype audio clips. The <b>cLogotypeAudio</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/7ce801bf-38fd-4490-8465-40ed5078bbff">CERT_LOGOTYPE_INFO</a>
 

 


---
UID: NC:cryptxml.PFN_CRYPT_XML_WRITE_CALLBACK
title: PFN_CRYPT_XML_WRITE_CALLBACK
author: windows-sdk-content
description: Writes XML data.
old-location: security\pfn_crypt_xml_write_callback.htm
tech.root: seccrypto
ms.assetid: 722f6ab4-ca6f-460d-9282-e4b7ca484077
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PFN_CRYPT_XML_WRITE_CALLBACK, PFN_CRYPT_XML_WRITE_CALLBACK callback, PFN_CRYPT_XML_WRITE_CALLBACK callback function [Security], cryptxml/PFN_CRYPT_XML_WRITE_CALLBACK, security.pfn_crypt_xml_write_callback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: cryptxml.h
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
 - UserDefined
api_location:
 - Cryptxml.h
api_name:
 - PFN_CRYPT_XML_WRITE_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CRYPT_XML_WRITE_CALLBACK callback function


## -description


The <i>PFN_CRYPT_XML_WRITE_CALLBACK</i> callback function writes XML data.


## -parameters




### -param *pvCallbackState [in, out]

A pointer to an argument that is passed to the callback function pointed to by the <i>pfnWrite</i> parameter of the <a href="https://msdn.microsoft.com/ef21897e-66f1-436c-8440-91422f5c95a7">CryptXmlDllEncodeAlgorithm</a> function.


### -param *pbData [in]

A pointer to a block of data to be written.


### -param cbData

The size, in bytes, of the data pointed to by the <i>pbData</i> parameter.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.




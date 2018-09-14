---
UID: NC:cryptxml.PFN_CRYPT_XML_DATA_PROVIDER_CLOSE
title: PFN_CRYPT_XML_DATA_PROVIDER_CLOSE
author: windows-sdk-content
description: Releases the data provider.
old-location: security\pfn_crypt_xml_data_provider_close.htm
tech.root: seccrypto
ms.assetid: 886fbe92-f9ab-49d4-968a-afeadbf2f030
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: PFN_CRYPT_XML_DATA_PROVIDER_CLOSE, PFN_CRYPT_XML_DATA_PROVIDER_CLOSE callback, PFN_CRYPT_XML_DATA_PROVIDER_CLOSE callback function [Security], cryptxml/PFN_CRYPT_XML_DATA_PROVIDER_CLOSE, security.pfn_crypt_xml_data_provider_close
ms.prod: windows
ms.technology: windows-sdk
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
 - PFN_CRYPT_XML_DATA_PROVIDER_CLOSE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CRYPT_XML_DATA_PROVIDER_CLOSE callback function


## -description


The <i>PFN_CRYPT_XML_DATA_PROVIDER_CLOSE</i> callback function releases the data provider.


## -parameters




### -param *pvCallbackState [in, out]

An application defined argument for the callback function.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.




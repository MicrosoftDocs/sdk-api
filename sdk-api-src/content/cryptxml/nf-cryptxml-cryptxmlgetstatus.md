---
UID: NF:cryptxml.CryptXmlGetStatus
title: CryptXmlGetStatus function
author: windows-sdk-content
description: Returns a CRYPT_XML_STATUS structure that contains status information about the object specified by the supplied handle.
old-location: security\cryptxmlgetstatus.htm
old-project: SecCrypto
ms.assetid: 685a87dc-36e9-464a-988e-de907d2dae41
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CryptXmlGetStatus, CryptXmlGetStatus function [Security], cryptxml/CryptXmlGetStatus, security.cryptxmlgetstatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: CRYPT_XML_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Cryptxml.dll
api_name:
-	CryptXmlGetStatus
product: Windows
targetos: Windows
req.lib: Cryptxml.lib
req.dll: Cryptxml.dll
req.irql: 
---

# CryptXmlGetStatus function


## -description


The <b>CryptXmlGetStatus</b> function returns a <a href="https://msdn.microsoft.com/1d49429e-9c81-4bf0-92d8-4effe9795dc9">CRYPT_XML_STATUS</a> structure that contains status information about the object specified by the supplied handle.


## -parameters




### -param hCryptXml

A handle to a <a href="https://msdn.microsoft.com/d9930946-aec0-42a4-949f-af8b2e9c6e6c">CRYPT_XML_SIGNATURE</a> structure, an array 
of <b>CRYPT_XML_SIGNATURE</b> structures , a <a href="https://msdn.microsoft.com/af16af5a-b1e5-4250-bdb1-f3fceb1830b9">CRYPT_XML_REFERENCE</a> structure, or a  Manifest object about which to get status information.


### -param pStatus

A pointer to a <a href="https://msdn.microsoft.com/1d49429e-9c81-4bf0-92d8-4effe9795dc9">CRYPT_XML_STATUS</a> structure to receive the returned status information. 


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.




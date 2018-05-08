---
UID: NE:msxml6._XHR_CERT_IGNORE_FLAG
title: "_XHR_CERT_IGNORE_FLAG"
author: windows-driver-content
description: Defines flags that you can assign to an outgoing HTTP request to ignore certain certificate errors by calling the SetProperty method on the IXMLHTTPRequest3 interface.
old-location: ixhr2\xhr_cert_ignore_flag.htm
old-project: ixhr2
ms.assetid: 22b7b3b0-a5e2-4cf1-af92-4fe66506fa40
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: XHR_CERT_IGNORE_ALL_SERVER_ERRORS, XHR_CERT_IGNORE_CERT_CN_INVALID, XHR_CERT_IGNORE_CERT_DATE_INVALID, XHR_CERT_IGNORE_FLAG, XHR_CERT_IGNORE_FLAG enumeration [XMLHttpRequest2], XHR_CERT_IGNORE_REVOCATION_FAILED, XHR_CERT_IGNORE_UNKNOWN_CA, _XHR_CERT_IGNORE_FLAG, ixhr2.xhr_cert_ignore_flag, msxml6/XHR_CERT_IGNORE_ALL_SERVER_ERRORS, msxml6/XHR_CERT_IGNORE_CERT_CN_INVALID, msxml6/XHR_CERT_IGNORE_CERT_DATE_INVALID, msxml6/XHR_CERT_IGNORE_FLAG, msxml6/XHR_CERT_IGNORE_REVOCATION_FAILED, msxml6/XHR_CERT_IGNORE_UNKNOWN_CA
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msxml.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Msxml.tlb
req.typenames: XHR_CERT_IGNORE_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	msxml6.h
api_name:
-	XHR_CERT_IGNORE_FLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: Msxml.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _XHR_CERT_IGNORE_FLAG enumeration


## -description


Defines flags that you can assign to an outgoing HTTP request to ignore certain certificate errors by calling the <a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">SetProperty</a> method on the <a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a>  interface.


## -enum-fields




### -field XHR_CERT_IGNORE_REVOCATION_FAILED

Ignore certificate revocation errors.


### -field XHR_CERT_IGNORE_UNKNOWN_CA

Ignore a certificate error for an unknown or invalid certificate authority.


### -field XHR_CERT_IGNORE_CERT_CN_INVALID

Ignore a certificate error caused by an invalid common name. This allows an invalid common name in a certificate where the server name specified by the app for the requested URL does not match the common name in the server certificate.


### -field XHR_CERT_IGNORE_CERT_DATE_INVALID

Ignore a certificate error caused by an invalid date in the certificate. This allows certificates that are expired or not yet effective.


### -field XHR_CERT_IGNORE_ALL_SERVER_ERRORS

Ignore all server certificate errors.


## -see-also




<a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a>



<a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">SetProperty</a>
 

 


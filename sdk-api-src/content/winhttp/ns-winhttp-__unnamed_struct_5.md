---
UID: NS:winhttp.__unnamed_struct_5
title: WINHTTP_CERTIFICATE_INFO
author: windows-sdk-content
description: The WINHTTP_CERTIFICATE_INFO structure contains certificate information returned from the server. This structure is used by the WinHttpQueryOption function.
old-location: http\internet_certificate_info.htm
old-project: winhttp
ms.assetid: 72b0094b-ac9d-499f-8a75-6728be2826ea
ms.author: windowssdkdev
ms.date: 03/09/2018
ms.keywords: WINHTTP_CERTIFICATE_INFO, WINHTTP_CERTIFICATE_INFO structure [HTTP], http.internet_certificate_info, winhttp/WINHTTP_CERTIFICATE_INFO, winhttp_internet_certificate_info_structure
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WINHTTP_CERTIFICATE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winhttp.h
api_name:
 - WINHTTP_CERTIFICATE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WINHTTP_CERTIFICATE_INFO structure


## -description


The <b>WINHTTP_CERTIFICATE_INFO</b> structure contains certificate information returned from the server. This structure is used by the 
<a href="https://msdn.microsoft.com/47973eab-de70-47bf-9713-97b87a500cfa">WinHttpQueryOption</a> function.


## -struct-fields




### -field ftExpiry

A 
						<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the date the certificate expires. 


### -field ftStart

A 
						<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the date the certificate becomes valid. 


### -field lpszSubjectInfo

A pointer to a buffer that contains the name of the organization, site, and server for which the certificate was issued. 


### -field lpszIssuerInfo

A pointer to a buffer that contains the name of the organization, site, and server that issued the certificate. 


### -field lpszProtocolName

A pointer to a buffer that contains the name of the protocol used to provide the secure connection. This member is not current used.


### -field lpszSignatureAlgName

A pointer to a buffer that contains the name of the algorithm used to sign the certificate. This member is not current used.


### -field lpszEncryptionAlgName

A pointer to a buffer that contains the name of the algorithm used to perform encryption over the secure channel (SSL/TLS) connection. This member is not current used.


### -field dwKeySize

The size, in bytes, of the key. 


## -remarks



The <b>WINHTTP_CERTIFICATE_INFO</b> structure contains information on the certificate returned by the server when the connection uses SSL/TLS. The <a href="https://msdn.microsoft.com/47973eab-de70-47bf-9713-97b87a500cfa">WinHttpQueryOption</a> function returns the <b>WINHTTP_CERTIFICATE_INFO</b> structure when the <i>dwOption</i> parameter passed to the <b>WinHttpQueryOption</b> function is set to <b>WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT</b>. For more information, see <a href="https://msdn.microsoft.com/2d0441f4-ddba-4f2a-8861-8803cad6f1ac">Option Flags</a>.

The <a href="https://msdn.microsoft.com/47973eab-de70-47bf-9713-97b87a500cfa">WinHttpQueryOption</a> function does not set  the <b>lpszProtocolName</b>, <b>lpszSignatureAlgName</b>, and <b>lpszEncryptionAlgName</b> members of the <b>WINHTTP_CERTIFICATE_INFO</b> structure, so these member are always returned as <b>NULL</b>.

Once the application no longer needs the returned <b>WINHTTP_CERTIFICATE_INFO</b> structure, the  <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function should be called to free any pointers returned in the structure. The structure members containing pointers that are not NULL and need to be freed are <b>lpszSubjectInfo</b> and <b>lpszIssuerInfo</b>.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Run-Time Requirements</a> section of the <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Windows HTTP Services</a> start page.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2d0441f4-ddba-4f2a-8861-8803cad6f1ac">Option Flags</a>



<a href="https://msdn.microsoft.com/b69e5087-7849-4cbc-a97b-204a26fdd044">WinHTTP
		  Versions</a>



<a href="https://msdn.microsoft.com/47973eab-de70-47bf-9713-97b87a500cfa">WinHttpQueryOption</a>
 

 


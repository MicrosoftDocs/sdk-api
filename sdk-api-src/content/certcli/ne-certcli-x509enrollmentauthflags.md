---
UID: NE:certcli.X509EnrollmentAuthFlags
title: X509EnrollmentAuthFlags
author: windows-sdk-content
description: Specifies the authentication type.
old-location: security\x509enrollmentauthflags.htm
tech.root: seccrypto
ms.assetid: 84a7e6e3-dfbb-4c27-af63-e521103e1b00
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: X509AuthAnonymous, X509AuthCertificate, X509AuthKerberos, X509AuthNone, X509AuthUsername, X509EnrollmentAuthFlags, X509EnrollmentAuthFlags enumeration [Security], certcli/X509AuthAnonymous, certcli/X509AuthCertificate, certcli/X509AuthKerberos, certcli/X509AuthNone, certcli/X509AuthUsername, certcli/X509EnrollmentAuthFlags, security.x509enrollmentauthflags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: certcli.h
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
 - HeaderDef
api_location:
 - Certcli.h
api_name:
 - X509EnrollmentAuthFlags
product: Windows
targetos: Windows
req.typenames: X509EnrollmentAuthFlags
req.redist: 
---

# X509EnrollmentAuthFlags enumeration


## -description


The <b>X509EnrollmentAuthFlags</b> enumeration specifies the authentication type.


## -enum-fields




### -field X509AuthNone

Reserved.


### -field X509AuthAnonymous

Anonymous authentication.


### -field X509AuthKerberos

Kerberos authentication.


### -field X509AuthUsername

Plaintext user name and password authentication.


### -field X509AuthCertificate

A client authentication certificate (suitable for <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">Secure Sockets Layer protocol</a> (SSL) client authentication) that is installed locally and that has an associated private key.  This certificate is used by the server to verify the client's identity.


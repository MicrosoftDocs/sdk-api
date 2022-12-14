---
UID: NE:certcli.X509EnrollmentAuthFlags
title: X509EnrollmentAuthFlags (certcli.h)
description: Specifies the authentication type.
helpviewer_keywords: ["X509AuthAnonymous","X509AuthCertificate","X509AuthKerberos","X509AuthNone","X509AuthUsername","X509EnrollmentAuthFlags","X509EnrollmentAuthFlags enumeration [Security]","certcli/X509AuthAnonymous","certcli/X509AuthCertificate","certcli/X509AuthKerberos","certcli/X509AuthNone","certcli/X509AuthUsername","certcli/X509EnrollmentAuthFlags","security.x509enrollmentauthflags"]
old-location: security\x509enrollmentauthflags.htm
tech.root: security
ms.assetid: 84a7e6e3-dfbb-4c27-af63-e521103e1b00
ms.date: 12/05/2018
ms.keywords: X509AuthAnonymous, X509AuthCertificate, X509AuthKerberos, X509AuthNone, X509AuthUsername, X509EnrollmentAuthFlags, X509EnrollmentAuthFlags enumeration [Security], certcli/X509AuthAnonymous, certcli/X509AuthCertificate, certcli/X509AuthKerberos, certcli/X509AuthNone, certcli/X509AuthUsername, certcli/X509EnrollmentAuthFlags, security.x509enrollmentauthflags
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
targetos: Windows
req.typenames: X509EnrollmentAuthFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X509EnrollmentAuthFlags
 - certcli/X509EnrollmentAuthFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Certcli.h
api_name:
 - X509EnrollmentAuthFlags
---

# X509EnrollmentAuthFlags enumeration


## -description

The <b>X509EnrollmentAuthFlags</b> enumeration specifies the authentication type.

## -enum-fields

### -field X509AuthNone:0

Reserved.

### -field X509AuthAnonymous:1

Anonymous authentication.

### -field X509AuthKerberos:2

Kerberos authentication.

### -field X509AuthUsername:4

Plaintext user name and password authentication.

### -field X509AuthCertificate:8

A client authentication certificate (suitable for <a href="/windows/desktop/SecGloss/s-gly">Secure Sockets Layer protocol</a> (SSL) client authentication) that is installed locally and that has an associated private key.  This certificate is used by the server to verify the client's identity.

---
UID: NN:mmcobj.Extensions
title: Extensions
author: windows-sdk-content
description: Represents a collection of Extension objects.
old-location: security\extensions.htm
old-project: SecCrypto
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: Extensions, Extensions object [Security], Extensions object [Security],described, mmcobj/Extensions, security.extensions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmcobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: "_ColumnSortOrder, COLUMNSORTORDER"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Capicom.dll
api_name:
 - Extensions
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: Capicom.dll
req.irql: 
req.product: GDI+ 1.1
---

# Extensions interface


## -description


<p class="CCE_Message">[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP. Instead, use the <a href="T:System.Security.Cryptography.X509Certificates.X509ExtensionCollection">X509ExtensionCollection Class</a> in the <a href="frlrfSystemSecurityCryptographyX509Certificates">System.Security.Cryptography.X509Certificates</a> namespace.]

The <b>Extensions</b> object represents a collection of <a href="https://msdn.microsoft.com/cca3121d-0f0f-4de2-a225-6dd3910078d7">Extension</a> objects. Each <a href="https://msdn.microsoft.com/cca3121d-0f0f-4de2-a225-6dd3910078d7">Extension</a> object represents a single certificate extension.


## -remarks



The <b>Extensions</b> object is returned by the <a href="https://msdn.microsoft.com/07793061-6f94-4467-bb01-aa65db657658">Certificate.Extensions</a> method.

The <b>Extensions</b> object cannot be created.




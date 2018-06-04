---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _CRYPTUI_CERT_MGR_STRUCT structure


## -description


The <b>CRYPTUI_CERT_MGR_STRUCT</b> structure contains information about a certificate manager dialog box.


## -struct-fields




### -field dwSize

The size, in bytes, of the structure. This value must be set to <code>sizeof(CRYPTUI_CERT_MGR_STRUCT)</code>.


### -field hwndParent

Handle of the parent window of the dialog box.


### -field dwFlags

Reserved. This value must be set to zero.


### -field pwszTitle

Title of the dialog box.


### -field pszInitUsageOID

Enhanced key usage <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the certificates that will initially appear in the dialog box. The default value is <b>NULL</b>, which displays all certificates.


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

# _WS_SUBJECT_NAME_CERT_CREDENTIAL structure


## -description



The type for specifying a certificate credential using the
certificate's subject name, store location and store name.  The
specified credential is loaded when the containing channel or listener
is opened.
            


## -struct-fields




### -field credential


The base type from which this type and all other certificate credential types derive.
                


### -field storeLocation


The certificate store location (such as CERT_SYSTEM_STORE_CURRENT_USER
or CERT_SYSTEM_STORE_LOCAL_MACHINE) that contains the specified
certificate.
                


### -field storeName


The certificate store name (such as "My") that contains the specified
certificate.
                


### -field subjectName


The subject name (such as "CN=service.com") of the specified
certificate.  The supplied subject name string must be in a format acceptable to
CERT_FIND_SUBJECT_NAME-based
search.
                (See <a href=" http://go.microsoft.com/fwlink/p/?linkid=139700">CertFindCertificateInStore</a>.)


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

# CryptUIDlgViewCertificateW function


## -description


The <b>CryptUIDlgViewCertificate</b> function presents a dialog box that displays a specified certificate.


## -parameters




### -param pCertViewInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/7bbd58df-3a1b-4d82-9a90-7c94260a7165">CRYPTUI_VIEWCERTIFICATE_STRUCT</a> structure that contains information about the certificate to view.


### -param pfPropertiesChanged [out]

Indicates whether any certificate properties were modified by the caller.


## -returns




						If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -see-also




<a href="https://msdn.microsoft.com/7bbd58df-3a1b-4d82-9a90-7c94260a7165">CRYPTUI_VIEWCERTIFICATE_STRUCT</a>
 

 


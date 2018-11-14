---
UID: NF:xenroll.IEnroll.AddExtensionsToRequest
title: IEnroll::AddExtensionsToRequest
author: windows-sdk-content
description: The AddExtensionsToRequest method adds extensions to the certificate request. This method was first defined in the IEnroll interface.
old-location: security\ienroll4_addextensionstorequest.htm
tech.root: seccrypto
ms.assetid: 6976fd52-98f0-4eff-aa83-7cf5cb5d5e67
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: AddExtensionsToRequest, AddExtensionsToRequest method [Security], AddExtensionsToRequest method [Security],IEnroll interface, IEnroll interface [Security],AddExtensionsToRequest method, IEnroll.AddExtensionsToRequest, IEnroll::AddExtensionsToRequest, security.ienroll4_addextensionstorequest, xenroll/IEnroll::AddExtensionsToRequest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll.AddExtensionsToRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xenroll.h
: 
- IEnroll.AddExtensionsToRequest
: 
---

# IEnroll::AddExtensionsToRequest


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>AddExtensionsToRequest</b> method adds extensions to the certificate request. This method was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.


## -parameters




### -param pCertExtensions [in]

A pointer to a <a href="https://msdn.microsoft.com/b393ef08-cedb-4840-a427-10ead315d6ea">CERT_EXTENSIONS</a> structure that represents the extensions to add to the request.


## -returns



The return value is an <b>HRESULT</b>, with S_OK returned if the call is successful.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 


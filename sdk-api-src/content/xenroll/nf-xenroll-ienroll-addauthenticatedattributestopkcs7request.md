---
UID: NF:xenroll.IEnroll.AddAuthenticatedAttributesToPKCS7Request
title: IEnroll::AddAuthenticatedAttributesToPKCS7Request
author: windows-sdk-content
description: The AddAuthenticatedAttributesToPKCS7Request method adds authenticated attributes to a PKCS #7 certificate request. This method was first defined in the IEnroll interface.
old-location: security\ienroll4_addauthenticatedattributestopkcs7request.htm
tech.root: seccrypto
ms.assetid: a65eca3d-8308-4bdc-b851-016a4e63a1f1
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: AddAuthenticatedAttributesToPKCS7Request, AddAuthenticatedAttributesToPKCS7Request method [Security], AddAuthenticatedAttributesToPKCS7Request method [Security],IEnroll interface, IEnroll interface [Security],AddAuthenticatedAttributesToPKCS7Request method, IEnroll.AddAuthenticatedAttributesToPKCS7Request, IEnroll::AddAuthenticatedAttributesToPKCS7Request, security.ienroll4_addauthenticatedattributestopkcs7request, xenroll/IEnroll::AddAuthenticatedAttributesToPKCS7Request
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
 - IEnroll.AddAuthenticatedAttributesToPKCS7Request
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll::AddAuthenticatedAttributesToPKCS7Request


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>AddAuthenticatedAttributesToPKCS7Request</b> method adds authenticated attributes to a PKCS #7 certificate request. This method was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.


## -parameters




### -param pAttributes [in]

A pointer to a <a href="https://msdn.microsoft.com/782f3022-d852-4ad7-8e0f-afbccc25928a">CRYPT_ATTRIBUTES</a> structure that represents the authenticated attributes to add to the PKCS #7 certificate request.


## -returns



The return value is an <b>HRESULT</b>, with S_OK returned if the call is successful.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 


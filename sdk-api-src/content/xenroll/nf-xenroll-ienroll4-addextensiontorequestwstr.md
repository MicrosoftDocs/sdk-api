---
UID: NF:xenroll.IEnroll4.addExtensionToRequestWStr
title: IEnroll4::addExtensionToRequestWStr
author: windows-sdk-content
description: Adds an extension to the request.
old-location: security\ienroll4_addextensiontorequestwstr.htm
tech.root: seccrypto
ms.assetid: 4ecca64b-a8f4-4816-8bf1-7b8e74262ac0
ms.author: windowssdkdev
ms.date: 12/04/2018
ms.keywords: IEnroll4 interface [Security],addExtensionToRequestWStr method, IEnroll4.addExtensionToRequestWStr, IEnroll4::addExtensionToRequestWStr, addExtensionToRequestWStr, addExtensionToRequestWStr method [Security], addExtensionToRequestWStr method [Security],IEnroll4 interface, security.ienroll4_addextensiontorequestwstr, xenroll/IEnroll4::addExtensionToRequestWStr
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
 - IEnroll4.addExtensionToRequestWStr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll4::addExtensionToRequestWStr


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addExtensionToRequestWStr</b> method adds an extension to the request. This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters




### -param Flags [in]

Specifies whether the extension is critical. 
If <b>TRUE</b>, the extension being added is critical. If <b>FALSE</b>, it is not critical.


### -param pwszName [in]

A pointer to a null-terminated wide character string that represents the Object Identifier (OID) for the extension name.


### -param pblobValue [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that represents the extension value.


## -returns



The return value is an <b>HRESULT</b>, with S_OK returned if the call is successful.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 


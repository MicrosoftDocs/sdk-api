---
UID: NF:xenroll.IEnroll2.EnumAlgs
title: IEnroll2::EnumAlgs
author: windows-sdk-content
description: Retrieves the IDs of cryptographic algorithms in a given algorithm class that are supported by the current cryptographic service provider (CSP).
old-location: security\ienroll4_enumalgs.htm
old-project: seccrypto
ms.assetid: a40d85d0-fd02-4e0a-af7d-dfefe02f4e2a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EnumAlgs, EnumAlgs method [Security], EnumAlgs method [Security],IEnroll2 interface, IEnroll2 interface [Security],EnumAlgs method, IEnroll2.EnumAlgs, IEnroll2::EnumAlgs, security.ienroll4_enumalgs, xenroll/IEnroll2::EnumAlgs
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll2.EnumAlgs
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll2::EnumAlgs


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>EnumAlgs</b> method retrieves the IDs of cryptographic algorithms in a given algorithm class that are supported by the current <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP).  This method was first defined in the <a href="https://msdn.microsoft.com/60a28944-35de-4ea2-8523-5634685ac224">IEnroll2</a> interface.


## -parameters




### -param dwIndex [in]

Specifies the ordinal position of the algorithm whose ID will be retrieved. Specify zero for the first algorithm.


### -param algClass [in]

A cryptographic algorithm class. The IDs returned by this method will be in the specified class. Specify one of the following:

<ul>
<li>ALG_CLASS_HASH</li>
<li>ALG_CLASS_KEY_EXCHANGE</li>
<li>ALG_CLASS_MSG_ENCRYPT</li>
<li>ALG_CLASS_DATA_ENCRYPT</li>
<li>ALG_CLASS_SIGNATURE</li>
</ul>

### -param pdwAlgID [out]

A pointer to LONG which receives a cryptographic algorithm ID which is supported by the current CSP.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. When there are no more algorithms to enumerate, the value ERROR_NO_MORE_ITEMS is returned.




## -remarks



For algorithm ID and class constants used by this method, see Wincrypt.h.




## -see-also




<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>



<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll2</a>
 

 


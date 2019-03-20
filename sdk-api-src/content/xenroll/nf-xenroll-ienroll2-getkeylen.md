---
UID: NF:xenroll.IEnroll2.GetKeyLen
title: IEnroll2::GetKeyLen (xenroll.h)
author: windows-sdk-content
description: The IEnroll4::GetKeyLen method retrieves the minimum and maximum key lengths for the signature and exchange keys.
old-location: security\ienroll4_getkeylen.htm
tech.root: SecCrypto
ms.assetid: ece7f5a3-e982-48b2-a249-a9c5b5a8a493
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetKeyLen, GetKeyLen method [Security], GetKeyLen method [Security],IEnroll2 interface, IEnroll2 interface [Security],GetKeyLen method, IEnroll2.GetKeyLen, IEnroll2::GetKeyLen, security.ienroll4_getkeylen, xenroll/IEnroll2::GetKeyLen
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
 - IEnroll2.GetKeyLen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll2::GetKeyLen


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GetKeyLen</b> method retrieves the minimum and maximum key lengths for the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">signature</a> and <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">exchange keys</a>. This method was first defined in the <a href="https://msdn.microsoft.com/60a28944-35de-4ea2-8523-5634685ac224">IEnroll2</a> interface. The values retrieved by this method are dependent upon the current <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a>.


## -parameters




### -param fMin [in]

Boolean value indicating which key length (minimum or maximum) is retrieved. If <i>fMin</i> is <b>TRUE</b>, the minimum key length is retrieved; if it is <b>FALSE</b>, the maximum key length is retrieved.


### -param fExchange [in]

Boolean value indicating the type of key. If <i>fExchange</i> is <b>TRUE</b>, the exchange key length is retrieved; if it is <b>FALSE</b>, the signature key length is retrieved.


### -param pdwKeySize [out]

Pointer that receives the key's minimum or maximum length, in bits.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success, and *<i>pdwKeySize</i> will be the value representing the length (in bits) for the key's minimum or maximum length.




## -remarks



Call this method to determine the minimum and maximum key lengths. If a CSP does not support this method, an error is returned.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll2</a>
 

 


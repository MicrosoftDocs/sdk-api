---
UID: NF:xenroll.IEnroll2.GetSupportedKeySpec
title: IEnroll2::GetSupportedKeySpec
author: windows-sdk-content
description: Retrieves information regarding the current cryptographic service provider (CSP) support for signature and/or exchange operations.
old-location: security\ienroll4_getsupportedkeyspec.htm
tech.root: seccrypto
ms.assetid: 8f7ace8e-0102-4c89-9d8a-e252ad60bb96
ms.author: windowssdkdev
ms.date: 12/04/2018
ms.keywords: GetSupportedKeySpec, GetSupportedKeySpec method [Security], GetSupportedKeySpec method [Security],IEnroll2 interface, IEnroll2 interface [Security],GetSupportedKeySpec method, IEnroll2.GetSupportedKeySpec, IEnroll2::GetSupportedKeySpec, security.ienroll4_getsupportedkeyspec, xenroll/IEnroll2::GetSupportedKeySpec
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
 - IEnroll2.GetSupportedKeySpec
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll2::GetSupportedKeySpec


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GetSupportedKeySpec</b> method retrieves information regarding the current <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) support for signature and/or exchange operations. This method was first defined in the <a href="https://msdn.microsoft.com/60a28944-35de-4ea2-8523-5634685ac224">IEnroll2</a> interface.

The values retrieved by this method are dependent upon the current CSP.


## -parameters




### -param pdwKeySpec [out]

A pointer to a <b>LONG</b> that receives a bit flag indicating whether the current CSP supports <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">exchange</a> and/or <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">signature keys</a>.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. If a CSP does not support this method, an error is returned.




## -remarks




Call this method to determine whether the current CSP supports exchange keys, signature keys, or both. The <i>pdwKeySpec</i> parameter will contain one or more of the following constants (defined in in Wincrypt.h):

<ul>
<li>AT_KEYEXCHANGE</li>
<li>AT_SIGNATURE.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll2</a>
 

 


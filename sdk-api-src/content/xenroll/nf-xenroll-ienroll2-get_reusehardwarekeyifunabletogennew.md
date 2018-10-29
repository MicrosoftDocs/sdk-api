---
UID: NF:xenroll.IEnroll2.get_ReuseHardwareKeyIfUnableToGenNew
title: IEnroll2::get_ReuseHardwareKeyIfUnableToGenNew
author: windows-sdk-content
description: The ReuseHardwareKeyIfUnableToGenNew property of IEnroll4 sets or retrieves a Boolean value that determines the action taken by the certificate enrollment control object if an error is encountered when generating a new key.
old-location: security\ienroll4_reusehardwarekeyifunabletogennew.htm
tech.root: seccrypto
ms.assetid: d67d47f2-9d89-44ba-a5de-e1ae2bc85673
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IEnroll2 interface [Security],ReuseHardwareKeyIfUnableToGenNew property, IEnroll2.ReuseHardwareKeyIfUnableToGenNew, IEnroll2.get_ReuseHardwareKeyIfUnableToGenNew, IEnroll2::ReuseHardwareKeyIfUnableToGenNew, IEnroll2::get_ReuseHardwareKeyIfUnableToGenNew, IEnroll2::put_ReuseHardwareKeyIfUnableToGenNew, IEnroll4 interface [Security],ReuseHardwareKeyIfUnableToGenNew property, IEnroll4.ReuseHardwareKeyIfUnableToGenNew, IEnroll4::get_ReuseHardwareKeyIfUnableToGenNew, IEnroll4::put_ReuseHardwareKeyIfUnableToGenNew, ReuseHardwareKeyIfUnableToGenNew property [Security], ReuseHardwareKeyIfUnableToGenNew property [Security],IEnroll2 interface, ReuseHardwareKeyIfUnableToGenNew property [Security],IEnroll4 interface, get_ReuseHardwareKeyIfUnableToGenNew, put_ReuseHardwareKeyIfUnableToGenNew, security.ienroll4_reusehardwarekeyifunabletogennew, xenroll/IEnroll2::ReuseHardwareKeyIfUnableToGenNew, xenroll/IEnroll2::get_ReuseHardwareKeyIfUnableToGenNew, xenroll/IEnroll2::put_ReuseHardwareKeyIfUnableToGenNew, xenroll/IEnroll4::ReuseHardwareKeyIfUnableToGenNew, xenroll/IEnroll4::get_ReuseHardwareKeyIfUnableToGenNew, xenroll/IEnroll4::put_ReuseHardwareKeyIfUnableToGenNew
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
 - IEnroll2.ReuseHardwareKeyIfUnableToGenNew
 - IEnroll2.get_ReuseHardwareKeyIfUnableToGenNew
 - IEnroll2.put_ReuseHardwareKeyIfUnableToGenNew
 - IEnroll4.ReuseHardwareKeyIfUnableToGenNew
 - IEnroll4.get_ReuseHardwareKeyIfUnableToGenNew
 - IEnroll4.put_ReuseHardwareKeyIfUnableToGenNew
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll2::get_ReuseHardwareKeyIfUnableToGenNew


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ReuseHardwareKeyIfUnableToGenNew</b> property sets or retrieves a Boolean value that determines the action taken by the 
certificate enrollment control object if an error is encountered when generating a new key.

This property was first defined in the <a href="https://msdn.microsoft.com/60a28944-35de-4ea2-8523-5634685ac224">IEnroll2</a> interface.

This property is read/write.


## -parameters


## -remarks



This property is a Boolean value. This property affects only <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service providers</a> (CSP) that return NTE_TOKEN_KEYSET_STORAGE_FULL. These CSPs are typically hardware-based; an example is a smart card. If this property is <b>TRUE</b> and an error is encountered while generating a new key, the certificate enrollment control object will reuse the existing hardware key. If this property is <b>FALSE</b> and an error is encountered while generating a new key, the certificate enrollment control object will not reuse the existing hardware key but will instead pass an error to the caller.




## -see-also




<a href="https://msdn.microsoft.com/60a28944-35de-4ea2-8523-5634685ac224">IEnroll2</a>



<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 


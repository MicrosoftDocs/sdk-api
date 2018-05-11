---
UID: NF:certexit.ICertExit2.GetManageModule
title: ICertExit2::GetManageModule
author: windows-driver-content
description: Retrieves the ICertManageModule interface associated with the ICertExit2 interface by calling GetManageModule and passing in the address of a pointer to an ICertManageModule.
old-location: security\icertexit2_getmanagemodule.htm
old-project: SecCrypto
ms.assetid: 7f0c1b63-fd09-43b9-9f88-fab154d94e94
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: CCertExit object [Security],GetManageModule method, GetManageModule, GetManageModule method [Security], GetManageModule method [Security],CCertExit object, GetManageModule method [Security],ICertExit2 interface, ICertExit2 interface [Security],GetManageModule method, ICertExit2.GetManageModule, ICertExit2::GetManageModule, certexit/ICertExit2::GetManageModule, security.icertexit2_getmanagemodule
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certexit.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certexit.h
api_name:
-	ICertExit2.GetManageModule
-	CCertExit.GetManageModule
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICertExit2::GetManageModule


## -description


The <b>GetManageModule</b> method retrieves the <a href="https://msdn.microsoft.com/82b7b770-c098-40da-8a4e-8eb0e0b8a645">ICertManageModule</a> interface associated with the <a href="https://msdn.microsoft.com/a9d66aeb-b596-4d50-9c07-b760cdf4f8c0">ICertExit2</a> interface by calling <b>GetManageModule</b> and passing in the address of a pointer to an <b>ICertManageModule</b>.


## -parameters




### -param ppManageModule [out]

Pointer to the <a href="https://msdn.microsoft.com/82b7b770-c098-40da-8a4e-8eb0e0b8a645">ICertManageModule</a> interface associated with the <a href="https://msdn.microsoft.com/a9d66aeb-b596-4d50-9c07-b760cdf4f8c0">ICertExit2</a> interface.


## -returns



<h3>C++</h3>
 The return value is an <b>HRESULT</b>. A value of S_OK indicates the method was successful.

<h3>VB</h3>
The return value is a <b>Variant</b> containing the <a href="https://msdn.microsoft.com/82b7b770-c098-40da-8a4e-8eb0e0b8a645">ICertManageModule</a> interface associated with the <a href="https://msdn.microsoft.com/a9d66aeb-b596-4d50-9c07-b760cdf4f8c0">ICertExit2</a> interface.




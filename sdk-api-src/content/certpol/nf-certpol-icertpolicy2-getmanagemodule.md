---
UID: NF:certpol.ICertPolicy2.GetManageModule
title: ICertPolicy2::GetManageModule
author: windows-sdk-content
description: Retrieves the ICertManageModule interface associated with the ICertPolicy2 interface by calling GetManageModule and passing in the address of a pointer to an ICertManageModule.
old-location: security\icertpolicy2_getmanagemodule.htm
tech.root: seccrypto
ms.assetid: a8d45938-1b89-4576-8705-7a174323e072
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CCertPolicy object [Security],GetManageModule method, GetManageModule, GetManageModule method [Security], GetManageModule method [Security],CCertPolicy object, GetManageModule method [Security],ICertPolicy2 interface, ICertPolicy2 interface [Security],GetManageModule method, ICertPolicy2.GetManageModule, ICertPolicy2::GetManageModule, _certsrv_icertpolicy2_getmanagemodule, certpol/ICertPolicy2::GetManageModule, security.icertpolicy2_getmanagemodule
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certpol.h
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
req.lib: Certidl.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certidl.lib
 - Certidl.dll
api_name:
 - ICertPolicy2.GetManageModule
 - CCertPolicy.GetManageModule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPolicy2::GetManageModule


## -description


The <b>GetManageModule</b> method retrieves the <a href="https://msdn.microsoft.com/82b7b770-c098-40da-8a4e-8eb0e0b8a645">ICertManageModule</a> interface associated with the <a href="https://msdn.microsoft.com/2e48b096-e23a-4106-bfaf-f089d2291fba">ICertPolicy2</a> interface by calling <b>GetManageModule</b> and passing in the address of a pointer to an <b>ICertManageModule</b>.


## -parameters




### -param ppManageModule [out]

Pointer to the <a href="https://msdn.microsoft.com/82b7b770-c098-40da-8a4e-8eb0e0b8a645">ICertManageModule</a> interface associated with the <a href="https://msdn.microsoft.com/2e48b096-e23a-4106-bfaf-f089d2291fba">ICertPolicy2</a> interface.


## -returns



<h3>C++</h3>
 The return value is an <b>HRESULT</b>. A value of S_OK indicates the method was successful.

<h3>VB</h3>
The return value is a <b>Variant</b> containing the <a href="https://msdn.microsoft.com/82b7b770-c098-40da-8a4e-8eb0e0b8a645">ICertManageModule</a> interface associated with the <a href="https://msdn.microsoft.com/2e48b096-e23a-4106-bfaf-f089d2291fba">ICertPolicy2</a> interface.




## -see-also




<b>CCertPolicy</b>



<a href="https://msdn.microsoft.com/2e48b096-e23a-4106-bfaf-f089d2291fba">ICertPolicy2</a>
 

 


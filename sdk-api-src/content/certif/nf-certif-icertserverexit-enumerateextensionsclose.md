---
UID: NF:certif.ICertServerExit.EnumerateExtensionsClose
title: ICertServerExit::EnumerateExtensionsClose
author: windows-sdk-content
description: Frees any resources connected with extension enumeration.
old-location: security\icertserverexit_enumerateextensionsclose.htm
tech.root: seccrypto
ms.assetid: 769235cd-d5ef-458b-a04b-88f9f831ce3f
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CCertServerExit object [Security],EnumerateExtensionsClose method, EnumerateExtensionsClose, EnumerateExtensionsClose method [Security], EnumerateExtensionsClose method [Security],CCertServerExit object, EnumerateExtensionsClose method [Security],ICertServerExit interface, ICertServerExit interface [Security],EnumerateExtensionsClose method, ICertServerExit.EnumerateExtensionsClose, ICertServerExit::EnumerateExtensionsClose, _certsrv_icertserverexit_enumerateextensionsclose, certif/ICertServerExit::EnumerateExtensionsClose, security.icertserverexit_enumerateextensionsclose
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certif.h
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
req.dll: Certcli.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertServerExit.EnumerateExtensionsClose
 - CCertServerExit.EnumerateExtensionsClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertServerExit::EnumerateExtensionsClose


## -description


The <b>EnumerateExtensionsClose</b>  method frees any resources connected with extension enumeration.

All applications that use <a href="https://msdn.microsoft.com/2a0c4919-b3a0-4027-85bd-970f6bc0cdeb">ICertServerExit::EnumerateExtensionsSetup</a> and <a href="https://msdn.microsoft.com/8726f5fa-dc85-4357-b73a-013842d6ab78">ICertServerExit::EnumerateExtensions</a> should call <b>EnumerateExtensionsClose</b> when finished enumerating.


## -parameters






## -see-also




<b>CCertServerExit</b>



<a href="https://msdn.microsoft.com/1554c09c-a7c1-44ad-9821-93c0913212fc">ICertServerExit</a>
 

 


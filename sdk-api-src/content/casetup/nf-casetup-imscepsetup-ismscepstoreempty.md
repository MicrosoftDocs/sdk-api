---
UID: NF:casetup.IMSCEPSetup.IsMSCEPStoreEmpty
title: IMSCEPSetup::IsMSCEPStoreEmpty
author: windows-sdk-content
description: Always returns VARIANT_TRUE. It should not be used.
old-location: security\imscepsetup_ismscepstoreempty.htm
tech.root: seccrypto
ms.assetid: 90ce2ea5-e531-4787-954a-cd4d09ba753e
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: IMSCEPSetup interface [Security],IsMSCEPStoreEmpty method, IMSCEPSetup.IsMSCEPStoreEmpty, IMSCEPSetup::IsMSCEPStoreEmpty, IsMSCEPStoreEmpty, IsMSCEPStoreEmpty method [Security], IsMSCEPStoreEmpty method [Security],IMSCEPSetup interface, casetup/IMSCEPSetup::IsMSCEPStoreEmpty, security.imscepsetup_ismscepstoreempty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - IMSCEPSetup.IsMSCEPStoreEmpty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSCEPSetup::IsMSCEPStoreEmpty


## -description


The <b>IsMSCEPStoreEmpty</b> method always returns <b>VARIANT_TRUE</b>. It should not be used.


## -parameters




### -param pbEmpty [out]

This parameter always contains <b>VARIANT_TRUE</b>.


## -remarks



For the Network Device Enrollment Service (NDES) role, the My personal store is used. The default implementation does not use a separate store for signing and exchange certificates.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb736404(v=VS.85).aspx">IMSCEPSetup</a>
 

 


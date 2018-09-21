---
UID: NF:casetup.ICertSrvSetup.GetExistingCACertificates
title: ICertSrvSetup::GetExistingCACertificates
author: windows-sdk-content
description: Gets the collection of CertSrvSetupKeyInformation objects that represent valid certification authority (CA) certificates currently installed on the computer.
old-location: security\icertsrvsetup_getexistingcacertificates.htm
tech.root: seccrypto
ms.assetid: fd8c7bac-b6db-41f2-a648-e01ebd09c41c
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: GetExistingCACertificates, GetExistingCACertificates method [Security], GetExistingCACertificates method [Security],ICertSrvSetup interface, ICertSrvSetup interface [Security],GetExistingCACertificates method, ICertSrvSetup.GetExistingCACertificates, ICertSrvSetup::GetExistingCACertificates, casetup/ICertSrvSetup::GetExistingCACertificates, security.icertsrvsetup_getexistingcacertificates
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - ICertSrvSetup.GetExistingCACertificates
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertSrvSetup::GetExistingCACertificates


## -description


The <b>GetExistingCACertificates</b> method gets the collection of <b>CertSrvSetupKeyInformation</b>  objects that represent valid <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) certificates currently installed on the computer. This method does not change the state of the <b>CCertSrvSetup</b> object.


## -parameters




### -param ppVal [out]

The address of a pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb736373(v=VS.85).aspx">ICertSrvSetupKeyInformationCollection</a> interface that can be used to access information for the set of valid CA certificates installed in the "LocalMachine" store.


## -remarks



The <b>CertSrvSetupKeyInformationCollection</b> object contains valid certificates. A certificate is considered valid if it satisfies the following criteria:

<ul>
<li>Contains an AT_SIGNATURE key that matches the key in the <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a> container.
</li>
<li>Is self-signed or has basic constraints for a CA.</li>
<li>Passes chain validation but might have an offline revocation error.
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb736371(v=VS.85).aspx">ICertSrvSetup</a>
 

 


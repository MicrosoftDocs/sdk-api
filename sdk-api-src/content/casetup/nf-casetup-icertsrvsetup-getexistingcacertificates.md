---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICertSrvSetup::GetExistingCACertificates


## -description


The <b>GetExistingCACertificates</b> method gets the collection of <b>CertSrvSetupKeyInformation</b>  objects that represent valid <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) certificates currently installed on the computer. This method does not change the state of the <b>CCertSrvSetup</b> object.


## -parameters




### -param ppVal [out]

The address of a pointer to an <a href="https://msdn.microsoft.com/d029dd5f-9c19-46fd-aac3-275c624a157b">ICertSrvSetupKeyInformationCollection</a> interface that can be used to access information for the set of valid CA certificates installed in the "LocalMachine" store.


## -remarks



The <b>CertSrvSetupKeyInformationCollection</b> object contains valid certificates. A certificate is considered valid if it satisfies the following criteria:

<ul>
<li>Contains an AT_SIGNATURE key that matches the key in the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> container.
</li>
<li>Is self-signed or has basic constraints for a CA.</li>
<li>Passes chain validation but might have an offline revocation error.
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/6792a0d6-d304-481d-a97b-5fb7033c7eae">ICertSrvSetup</a>
 

 


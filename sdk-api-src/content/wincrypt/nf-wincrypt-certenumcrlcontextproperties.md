---
UID: NF:wincrypt.CertEnumCRLContextProperties
title: CertEnumCRLContextProperties function
author: windows-sdk-content
description: The CertEnumCRLContextProperties function retrieves the first or next extended property associated with a certificate revocation list (CRL) context.
old-location: security\certenumcrlcontextproperties.htm
old-project: SecCrypto
ms.assetid: 330808ef-9b39-4bd4-ba0b-9e70ec516f33
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CertEnumCRLContextProperties, CertEnumCRLContextProperties function [Security], _crypto2_certenumcrlcontextproperties, security.certenumcrlcontextproperties, wincrypt/CertEnumCRLContextProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertEnumCRLContextProperties
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertEnumCRLContextProperties function


## -description


The <b>CertEnumCRLContextProperties</b> function retrieves the first or next extended property associated with a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) context. Used in a loop, this function can retrieve in sequence all extended properties associated with a CRL context.


## -parameters




### -param pCrlContext [in]

A pointer to a 
<a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a> structure.


### -param dwPropId [in]

Property number of the last property enumerated. To get the first property, <i>dwPropId</i> is zero. To retrieve subsequent properties, <i>dwPropId</i> is set to the property number returned by the last call to the function. To enumerate all the properties, function calls continue until the function returns zero. 




Applications can call 
<a href="https://msdn.microsoft.com/16c2cc06-28fd-42d9-a377-0df2eaeeae56">CertGetCRLContextProperty</a> with the <i>dwPropId</i> returned by this function to retrieve that property's data.


## -returns



The return value is a <b>DWORD</b> value that identifies a CRL context's property. The <b>DWORD</b> value returned by one call of the function can be supplied as the <i>dwPropId</i> in a subsequent call to the function. If there are no more properties to be enumerated or if the function fails, zero is returned.




## -see-also




<a href="https://msdn.microsoft.com/16c2cc06-28fd-42d9-a377-0df2eaeeae56">CertGetCRLContextProperty</a>



<a href="https://msdn.microsoft.com/library/Aa380252(v=VS.85).aspx">Extended Property Functions</a>
 

 


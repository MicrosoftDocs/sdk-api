---
UID: NF:wincrypt.CertEnumCTLContextProperties
title: CertEnumCTLContextProperties function
author: windows-sdk-content
description: The CertEnumCTLContextProperties function retrieves the first or next extended property associated with a certificate trust list (CTL) context. Used in a loop, this function can retrieve in sequence all extended properties associated with a CTL context.
old-location: security\certenumctlcontextproperties.htm
old-project: SecCrypto
ms.assetid: f5c9c4cd-bf99-41bf-b13e-f1921b011039
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CertEnumCTLContextProperties, CertEnumCTLContextProperties function [Security], _crypto2_certenumctlcontextproperties, security.certenumctlcontextproperties, wincrypt/CertEnumCTLContextProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - CertEnumCTLContextProperties
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertEnumCTLContextProperties function


## -description


The <b>CertEnumCTLContextProperties</b> function retrieves the first or next extended property associated with a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL) context. Used in a loop, this function can retrieve in sequence all extended properties associated with a CTL context.


## -parameters




### -param pCtlContext [in]

A pointer to a 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> structure.


### -param dwPropId [in]

Property number of the last property enumerated. To get the first property, <i>dwPropId</i> is zero. To retrieve subsequent properties, <i>dwPropId</i> is set to the property number returned by the last call to the function. To enumerate all the properties, function calls continue until the function returns zero. 




Applications can call 
<a href="https://msdn.microsoft.com/16e45fe1-2710-4fa1-82da-c298645d7379">CertGetCTLContextProperty</a> with the <i>dwPropId</i> returned by this function to retrieved that property's data.


## -returns



The return value is a <b>DWORD</b> value that identifies a CTL context's property. The <b>DWORD</b> value returned by one call of the function can be supplied as the <i>dwPropId</i> in a subsequent call to the function. If there are no more properties to be enumerated or if the function fails, zero is returned.




## -see-also




<a href="https://msdn.microsoft.com/16e45fe1-2710-4fa1-82da-c298645d7379">CertGetCTLContextProperty</a>



<a href="cryptography_functions.htm">Extended Property Functions</a>
 

 


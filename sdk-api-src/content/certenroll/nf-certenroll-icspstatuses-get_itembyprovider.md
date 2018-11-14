---
UID: NF:certenroll.ICspStatuses.get_ItemByProvider
title: ICspStatuses::get_ItemByProvider
author: windows-sdk-content
description: Retrieves an ICspStatus object that has the same name as the provider specified on input but identifies an algorithm that supports a different intended key use.
old-location: security\icspstatuses_itembyprovider_property.htm
tech.root: SecCertEnroll
ms.assetid: 6f6e29b3-4d20-44dc-9a9c-c68b6631a83f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICspStatuses interface [Security],ItemByProvider property, ICspStatuses.ItemByProvider, ICspStatuses.get_ItemByProvider, ICspStatuses::ItemByProvider, ICspStatuses::get_ItemByProvider, ItemByProvider property [Security], ItemByProvider property [Security],ICspStatuses interface, certenroll/ICspStatuses::ItemByProvider, certenroll/ICspStatuses::get_ItemByProvider, get_ItemByProvider, security.icspstatuses_itembyprovider_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspStatuses.ItemByProvider
 - ICspStatuses.get_ItemByProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- ICspStatuses.get_ItemByProvider
: 
---

# ICspStatuses::get_ItemByProvider


## -description


The <b>ItemByProvider</b>  property retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a> object that has the same name as the  provider specified on input but identifies an algorithm that supports a different intended key use.

This property is read-only.


## -parameters


## -remarks



The <b>ItemByProvider</b>  property retrieves the <a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a> object that matches the name of the input provider but is associated with a different <a href="https://msdn.microsoft.com/en-us/library/Aa379409(v=VS.85).aspx">X509KeySpec</a> enumeration value. For example, if the input provider has a <a href="https://msdn.microsoft.com/en-us/library/Aa376751(v=VS.85).aspx">KeySpec</a> value of XCN_AT_KEYEXCHANGE, the <b>ItemByProvider</b> property attempts to find an <b>ICspStatus</b> object for the same provider but with a <b>KeySpec</b> value of XCN_AT_SIGNATURE.

Because the <a href="https://msdn.microsoft.com/en-us/library/Aa376751(v=VS.85).aspx">KeySpec</a> property is only associated with legacy providers, if you specify a Cryptography API: Next Generation (CNG) providers, the <b>ItemByProvider</b>  property returns the same <a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a> object as that entered.

To use this property to iterate through the collection, perform the following steps:<ul>
<li>Retrieve an <a href="https://msdn.microsoft.com/en-us/library/Aa376761(v=VS.85).aspx">ICspStatuses</a> collection by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa965815(v=VS.85).aspx">GetCspStatuses</a> method or the <a href="https://msdn.microsoft.com/en-us/library/Aa377517(v=VS.85).aspx">CspStatuses</a> property on the <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a> interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/41ccbe27-165d-42d1-95b4-0b96565818aa">ItemByIndex</a> property to iterate through the collection.</li>
<li>For each <a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a> element retrieved that contains the provider you are interested in, call <b>ItemByProvider</b>.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376761(v=VS.85).aspx">ICspStatuses</a>
 

 


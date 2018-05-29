---
UID: NF:windns.DnsFree
title: DnsFree function
author: windows-sdk-content
description: Frees memory allocated for DNS records that was obtained using the DnsQuery function.
old-location: dns\dnsfree.htm
old-project: DNS
ms.assetid: 32baa672-2106-4c4a-972a-f7f79996b613
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: DnsFree, DnsFree function [DNS], dns.dnsfree, windns/DnsFree
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: windns.h
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
req.typenames: DNS_FREE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dnsapi.dll
api_name:
-	DnsFree
product: Windows
targetos: Windows
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DnsFree function


## -description


The <b>DnsFree</b> function frees memory allocated for DNS records that was obtained using the 
<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a> function.


## -parameters




### -param pData [in, out]

A pointer to the DNS data to be freed.


### -param FreeType [in]

A value that specifies the type of DNS data in <i>pData</i>. For more information and a list of values, see the <a href="https://msdn.microsoft.com/976982a1-08f1-4c67-b823-1eea34f0c643">DNS_FREE_TYPE</a> enumeration.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/976982a1-08f1-4c67-b823-1eea34f0c643">DNS_FREE_TYPE</a>
 

 


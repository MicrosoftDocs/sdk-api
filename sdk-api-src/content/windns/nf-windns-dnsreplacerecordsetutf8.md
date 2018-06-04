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

# DnsReplaceRecordSetUTF8 function


## -description


The 
<b>DnsReplaceRecordSet</b> function type replaces an existing resource record (RR) set. Like many DNS functions, the 
<b>DnsReplaceRecordSet</b> function type is implemented in multiple forms to facilitate different character encoding, which is indicated by a suffix. Based on the character encoding involved, use one of the following functions:

<b>DnsReplaceRecordSetA</b> (_A for ANSI encoding)

<b>DnsReplaceRecordSetW</b> (_W for Unicode encoding)

<b>DnsReplaceRecordSetUTF8</b> (_UTF8 for UTF 8 encoding)

Be aware of the lack of an underscore between the function type name and its suffix. If the 
<b>DnsReplaceRecordSet</b> function type is called without its suffix (A, W, or UTF8), a compiler error will occur.


## -parameters




### -param pReplaceSet

TBD


### -param Options [in]

A value that contains a bitmap of <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Update  Options</a>. Options can be combined and all options override <b>DNS_UPDATE_SECURITY_USE_DEFAULT</b>.


### -param hContext [in, optional]

The handle to the credentials of a specific account. Used when secure dynamic update is required. This parameter is optional.


### -param pExtraInfo [in, out, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.


### -param pReserved [in, out, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.


#### - pNewSet [in]

A pointer to a 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure that contains the RR set that replaces the existing set. The specified RR set is replaced with the contents of <i>pNewSet</i>. To delete a RR set, specify the set in <i>pNewSet</i>, but set <i>RDATA</i> to <b>NULL</b>.


## -returns



Returns success confirmation upon successful completion. Otherwise, returns the appropriate DNS-specific error code as defined in Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>



<a href="https://msdn.microsoft.com/4287b4e1-a7a2-4b73-b5bb-21bc639bae73">DnsModifyRecordsInSet</a>
 

 


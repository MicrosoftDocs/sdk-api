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

# DsQuoteRdnValueA function


## -description


The <b>DsQuoteRdnValue</b> function converts an RDN into a quoted RDN value, if the RDN value contains characters that require quotes. The quoted RDN can then be submitted as part of a distinguished name (DN) to the directory service using various APIs such as LDAP. An example of an RDN that would require quotes would be one that has a comma-separated value, such as an RDN for a name that uses the format "last,first".


## -parameters




### -param cUnquotedRdnValueLength [in]

The number of characters in the <i>psUnquotedRdnValue</i> string.


### -param psUnquotedRdnValue [in]

The string that specifies the unquoted RDN value.


### -param pcQuotedRdnValueLength [in, out]

The maximum number of characters in the <i>psQuotedRdnValue</i> string.

The following flags are the output for this parameter.



#### ERROR_SUCCESS

Indicates that the correct number of characters were found in <i>psQuotedRdnValue</i>.



#### ERROR_BUFFER_OVERFLOW

Indicates that the number of characters in the string do not match <i>psQuotedRdnValue</i>.


### -param psQuotedRdnValue [out]

The string that receives the converted, and perhaps quoted, RDN value.


## -returns



The following list contains the possible values  returned for the <b>DsQuoteRdnValue</b> function.




## -remarks



Quotes are not added to the RDN if none are required. In this case, the output RDN value is the same as the input RDN value.

When quoting is required, the RDN is quoted in accordance with the specification "Lightweight Directory Access Protocol (v3): UTF-8 String Representation of Distinguished Names," RFC 2253.

The input and output RDN values are not <b>NULL</b>-terminated strings.

To revert changes made by this call, call the <a href="https://msdn.microsoft.com/6e3dd220-ba98-46b5-8522-93cbe2029aa4">DsUnquoteRdnValue</a> function.




## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/6e3dd220-ba98-46b5-8522-93cbe2029aa4">DsUnquoteRdnValue</a>
 

 


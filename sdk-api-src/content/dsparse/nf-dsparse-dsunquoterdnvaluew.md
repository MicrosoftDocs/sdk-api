---
UID: NF:dsparse.DsUnquoteRdnValueW
title: DsUnquoteRdnValueW function
author: windows-sdk-content
description: The DsUnquoteRdnValue function is a client call that converts a quoted RDN value back to an unquoted RDN value.
old-location: ad\dsunquoterdnvalue.htm
tech.root: AD
ms.assetid: 6e3dd220-ba98-46b5-8522-93cbe2029aa4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DsUnquoteRdnValue, DsUnquoteRdnValue function [Active Directory], DsUnquoteRdnValueA, DsUnquoteRdnValueW, ERROR_BUFFER_OVERFLOW, ERROR_SUCCESS, _glines_dsunquoterdnvalue, ad.dsunquoterdnvalue, dsparse/DsUnquoteRdnValue, dsparse/DsUnquoteRdnValueA, dsparse/DsUnquoteRdnValueW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dsparse.h
req.include-header: Ntdsapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsUnquoteRdnValueW (Unicode) and DsUnquoteRdnValueA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsUnquoteRdnValue
 - DsUnquoteRdnValueA
 - DsUnquoteRdnValueW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsUnquoteRdnValueW function


## -description


The <b>DsUnquoteRdnValue</b> function is a client call that converts a quoted RDN value back to an unquoted RDN value. Because the RDN was originally put into quotes because it contained characters that could be misinterpreted when it was embedded within a distinguished name (DN), the unquoted RDN value should not be submitted as part of a DN to the directory service using various APIs such as LDAP.


## -parameters




### -param cQuotedRdnValueLength [in]

The number of characters in the <i>psQuotedRdnValue</i> string.


### -param psQuotedRdnValue [in]

The RDN value that may be quoted and escaped.


### -param pcUnquotedRdnValueLength [in, out]

The input value for this argument is the maximum length, in characters, of <i>psQuotedRdnValue</i>.

The output value for this argument includes the following flags.



#### ERROR_SUCCESS

This is returned if the number of characters match the string used in <i>psQuotedRdnValue</i>.



#### ERROR_BUFFER_OVERFLOW

This is returned if the number of characters do not match the string used in <i>psQuotedRdnValue</i>.


### -param psUnquotedRdnValue [out]

The converted, unquoted RDN value.


##### - pcUnquotedRdnValueLength.ERROR_BUFFER_OVERFLOW

This is returned if the number of characters do not match the string used in <i>psQuotedRdnValue</i>.


##### - pcUnquotedRdnValueLength.ERROR_SUCCESS

This is returned if the number of characters match the string used in <i>psQuotedRdnValue</i>.


## -returns



The following list contains the possible values that are returned for the <b>DsUnquoteRdnValue</b> function.




## -remarks



When <i>psQuotedRdnValue</i> is quoted:

<ul>
<li>The leading and trailing quotes are removed.</li>
<li>White space before the first quote is discarded.</li>
<li>White space trailing the last quote is discarded.</li>
<li>Escapes are removed and the character following the escape is kept.</li>
</ul>
The following actions are taken when <i>psQuotedRdnValue</i> is unquoted:

<ul>
<li>The leading white space is discarded.</li>
<li>The trailing white space is kept.</li>
<li>Escaped non-special characters return an error.</li>
<li>Unescaped special characters return an error.</li>
<li>RDN values beginning with # (ignoring leading white space) are handled as a  BER value that has previously been converted to a string, and converted accordingly.</li>
<li>Escaped hex digits (\89) are converted into a binary byte (0x89).</li>
<li>Escapes are removed from escaped special characters.</li>
</ul>
The following actions are always taken:

<ul>
<li>Escaped special characters are unescaped.</li>
<li>The input and output RDN values are not null-terminated values.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/a1e8a4c0-965a-4061-aab3-3e719ec6374d">DsQuoteRdnValue</a>
 

 


---
UID: NF:dsparse.DsQuoteRdnValueA
title: DsQuoteRdnValueA function (dsparse.h)
description: Converts an RDN into a quoted RDN value, if the RDN value contains characters that require quotes. (ANSI)
helpviewer_keywords: ["DsQuoteRdnValueA", "ERROR_BUFFER_OVERFLOW", "ERROR_SUCCESS", "dsparse/DsQuoteRdnValueA"]
old-location: ad\dsquoterdnvalue.htm
tech.root: ad
ms.assetid: a1e8a4c0-965a-4061-aab3-3e719ec6374d
ms.date: 12/05/2018
ms.keywords: DsQuoteRdnValue, DsQuoteRdnValue function [Active Directory], DsQuoteRdnValueA, DsQuoteRdnValueW, ERROR_BUFFER_OVERFLOW, ERROR_SUCCESS, _glines_dsquoterdnvalue, ad.dsquoterdnvalue, dsparse/DsQuoteRdnValue, dsparse/DsQuoteRdnValueA, dsparse/DsQuoteRdnValueW
req.header: dsparse.h
req.include-header: Ntdsapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsQuoteRdnValueW (Unicode) and DsQuoteRdnValueA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsQuoteRdnValueA
 - dsparse/DsQuoteRdnValueA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsQuoteRdnValue
 - DsQuoteRdnValueA
 - DsQuoteRdnValueW
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

To revert changes made by this call, call the <a href="/windows/desktop/api/dsparse/nf-dsparse-dsunquoterdnvaluea">DsUnquoteRdnValue</a> function.





> [!NOTE]
> The dsparse.h header defines DsQuoteRdnValue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/dsparse/nf-dsparse-dsunquoterdnvaluea">DsUnquoteRdnValue</a>

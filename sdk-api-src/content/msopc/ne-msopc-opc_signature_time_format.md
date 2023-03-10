---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0001_0076_0005
title: OPC_SIGNATURE_TIME_FORMAT (msopc.h)
description: Describes how to interpret the signingTime parameter, which is a record of when a signature was created, of the IOpcDigitalSignature::GetSigningTime method.
helpviewer_keywords: ["OPC_SIGNATURE_TIME_FORMAT","OPC_SIGNATURE_TIME_FORMAT enumeration [Open Packaging Conventions]","OPC_SIGNATURE_TIME_FORMAT_DAYS","OPC_SIGNATURE_TIME_FORMAT_MILLISECONDS","OPC_SIGNATURE_TIME_FORMAT_MINUTES","OPC_SIGNATURE_TIME_FORMAT_MONTHS","OPC_SIGNATURE_TIME_FORMAT_SECONDS","OPC_SIGNATURE_TIME_FORMAT_YEARS","msopc/OPC_SIGNATURE_TIME_FORMAT","msopc/OPC_SIGNATURE_TIME_FORMAT_DAYS","msopc/OPC_SIGNATURE_TIME_FORMAT_MILLISECONDS","msopc/OPC_SIGNATURE_TIME_FORMAT_MINUTES","msopc/OPC_SIGNATURE_TIME_FORMAT_MONTHS","msopc/OPC_SIGNATURE_TIME_FORMAT_SECONDS","msopc/OPC_SIGNATURE_TIME_FORMAT_YEARS","opc.opc_signature_time_format"]
old-location: opc\opc_signature_time_format.htm
tech.root: OPC
ms.assetid: 9b8ff585-5795-48ce-b2fd-a49e3d34ccb9
ms.date: 12/05/2018
ms.keywords: OPC_SIGNATURE_TIME_FORMAT, OPC_SIGNATURE_TIME_FORMAT enumeration [Open Packaging Conventions], OPC_SIGNATURE_TIME_FORMAT_DAYS, OPC_SIGNATURE_TIME_FORMAT_MILLISECONDS, OPC_SIGNATURE_TIME_FORMAT_MINUTES, OPC_SIGNATURE_TIME_FORMAT_MONTHS, OPC_SIGNATURE_TIME_FORMAT_SECONDS, OPC_SIGNATURE_TIME_FORMAT_YEARS, msopc/OPC_SIGNATURE_TIME_FORMAT, msopc/OPC_SIGNATURE_TIME_FORMAT_DAYS, msopc/OPC_SIGNATURE_TIME_FORMAT_MILLISECONDS, msopc/OPC_SIGNATURE_TIME_FORMAT_MINUTES, msopc/OPC_SIGNATURE_TIME_FORMAT_MONTHS, msopc/OPC_SIGNATURE_TIME_FORMAT_SECONDS, msopc/OPC_SIGNATURE_TIME_FORMAT_YEARS, opc.opc_signature_time_format
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OpcDigitalSignature.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OPC_SIGNATURE_TIME_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msopc_0001_0076_0005
 - msopc/__MIDL___MIDL_itf_msopc_0001_0076_0005
 - OPC_SIGNATURE_TIME_FORMAT
 - msopc/OPC_SIGNATURE_TIME_FORMAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msopc.h
api_name:
 - OPC_SIGNATURE_TIME_FORMAT
---

# OPC_SIGNATURE_TIME_FORMAT enumeration


## -description

Describes how to interpret the <i>signingTime</i> parameter, which is a record of when a signature was created,  of the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsigningtime">IOpcDigitalSignature::GetSigningTime</a> method.

## -enum-fields

### -field OPC_SIGNATURE_TIME_FORMAT_MILLISECONDS:0

The format is the complete date with hours, minutes, and seconds expressed as a decimal fraction.

Syntax: <i>YYYY</i>-<i>MM</i>-<i>DD</i>T<i>hh</i>:<i>mm</i>:<i>ss</i>.<i>s</i><i>TZD</i>

A value of "2010-03-09T18:45:32.3-08:00" would represent 6:45:32.3 P.M. on March 9, 2010 Pacific Time.

### -field OPC_SIGNATURE_TIME_FORMAT_SECONDS:1

The format is the complete date with hours, minutes, and seconds.

Syntax: <i>YYYY</i>-<i>MM</i>-<i>DD</i>T<i>hh</i>:<i>mm</i>:<i>ss</i><i>TZD</i>

A value of "2010-03-09T18:45:32-08:00" would represent 6:45:32 P.M. on March 9, 2010  Pacific Time.

### -field OPC_SIGNATURE_TIME_FORMAT_MINUTES:2

The format is the complete date with hours and  minutes.

Syntax: <i>YYYY</i>-<i>MM</i>-<i>DD</i>T<i>hh</i>:<i>mm</i><i>TZD</i>

A value of "2010-03-09T18:45-08:00" would represent 6:45 P.M. on March 9, 2010 Pacific Time.

### -field OPC_SIGNATURE_TIME_FORMAT_DAYS:3

The format is the complete date.

Syntax: <i>YYYY</i>-<i>MM</i>-<i>DD</i>

A value of "2010-03-09" would represent March 9, 2010.

### -field OPC_SIGNATURE_TIME_FORMAT_MONTHS:4

The format is the year and month.

Syntax: <i>YYYY</i>-<i>MM</i>

A value of "2010-03" would represent March, 2010.

### -field OPC_SIGNATURE_TIME_FORMAT_YEARS:5

The format is the year.

Syntax:  <i>YYYY</i>

A value of "2010" would represent 2010.

## -remarks

The following table provides descriptions of  placeholder values.

<table>
<tr>
<th>Placeholder </th>
<th>Description </th>
<th>Example</th>
</tr>
<tr>
<td>
<i>YYYY</i>

</td>
<td>
Four-digit year.

</td>
<td>
2010

</td>
</tr>
<tr>
<td>
<i>MM</i>

</td>
<td>
Two-digit month with a leading zero. Possible values: 01–12.

</td>
<td>
03

</td>
</tr>
<tr>
<td>
<i>DD</i>

</td>
<td>
Two-digit day of month with a leading zero. Possible values: 01–31.

</td>
<td>
09

</td>
</tr>
<tr>
<td>
<i>hh</i>

</td>
<td>
Two-digit hour, 24-hour time with a leading zero. Possible values: 00–23.

</td>
<td>
18

</td>
</tr>
<tr>
<td>
<i>mm</i>

</td>
<td>
Two-digit minute with a leading zero. Possible values: 00–59.

</td>
<td>
45

</td>
</tr>
<tr>
<td>
<i>ss</i>

</td>
<td>
Two-digit second with a leading zero. Possible values: 00–59.

</td>
<td>
32

</td>
</tr>
<tr>
<td>
<i>s</i>

</td>
<td>
One digit representing the decimal fraction of a second.

</td>
<td>
3

</td>
</tr>
<tr>
<td>
<i>TZD</i>

</td>
<td>
Time zone designator with a leading zero. Possible values:  Z, +<i>hh</i>:<i>mm</i>, -<i>hh</i>:<i>mm</i>.

</td>
<td>
-08:00

</td>
</tr>
</table>

## -see-also

<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-gettimeformat">IOpcDigitalSignature::GetTimeFormat</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-gettimeformat">IOpcSigningOptions::GetTimeFormat</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-settimeformat">IOpcSigningOptions::SetTimeFormat</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-enumerations">Packaging Enumerations</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>



<a href="https://www.w3.org/TR/xmldsig-core/">W3C Recommendation, XML Signature and Syntax Processing</a>

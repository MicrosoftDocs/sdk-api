---
UID: NS:tdh._PAYLOAD_FILTER_PREDICATE
title: PAYLOAD_FILTER_PREDICATE (tdh.h)
description: Defines an event payload filter predicate that describes how to filter on a single field in a trace session.
helpviewer_keywords: ["*PPAYLOAD_FILTER_PREDICATE","PAYLOADFIELD_BETWEEN","PAYLOADFIELD_CONTAINS","PAYLOADFIELD_DOESNTCONTAIN","PAYLOADFIELD_EQ","PAYLOADFIELD_GE","PAYLOADFIELD_GT","PAYLOADFIELD_INVALID","PAYLOADFIELD_IS","PAYLOADFIELD_ISNOT","PAYLOADFIELD_LE","PAYLOADFIELD_LT","PAYLOADFIELD_MODULO","PAYLOADFIELD_NE","PAYLOADFIELD_NOTBETWEEN","PAYLOAD_FILTER_PREDICATE","PAYLOAD_FILTER_PREDICATE structure [ETW]","PPAYLOAD_FILTER_PREDICATE","PPAYLOAD_FILTER_PREDICATE structure pointer [ETW]","etw.payload_filter_predicate","tdh/PAYLOAD_FILTER_PREDICATE","tdh/PPAYLOAD_FILTER_PREDICATE"]
old-location: etw\payload_filter_predicate.htm
tech.root: ETW
ms.assetid: 6B8C03C9-2936-4FEE-AEF4-ABC368B1CB75
ms.date: 12/05/2018
ms.keywords: '*PPAYLOAD_FILTER_PREDICATE, PAYLOADFIELD_BETWEEN, PAYLOADFIELD_CONTAINS, PAYLOADFIELD_DOESNTCONTAIN, PAYLOADFIELD_EQ, PAYLOADFIELD_GE, PAYLOADFIELD_GT, PAYLOADFIELD_INVALID, PAYLOADFIELD_IS, PAYLOADFIELD_ISNOT, PAYLOADFIELD_LE, PAYLOADFIELD_LT, PAYLOADFIELD_MODULO, PAYLOADFIELD_NE, PAYLOADFIELD_NOTBETWEEN, PAYLOAD_FILTER_PREDICATE, PAYLOAD_FILTER_PREDICATE structure [ETW], PPAYLOAD_FILTER_PREDICATE, PPAYLOAD_FILTER_PREDICATE structure pointer [ETW], etw.payload_filter_predicate, tdh/PAYLOAD_FILTER_PREDICATE, tdh/PPAYLOAD_FILTER_PREDICATE'
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PAYLOAD_FILTER_PREDICATE, *PPAYLOAD_FILTER_PREDICATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PAYLOAD_FILTER_PREDICATE
 - tdh/_PAYLOAD_FILTER_PREDICATE
 - PPAYLOAD_FILTER_PREDICATE
 - tdh/PPAYLOAD_FILTER_PREDICATE
 - PAYLOAD_FILTER_PREDICATE
 - tdh/PAYLOAD_FILTER_PREDICATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tdh.h
api_name:
 - PAYLOAD_FILTER_PREDICATE
---

# PAYLOAD_FILTER_PREDICATE structure


## -description

Defines an event payload filter predicate that describes how to filter on a single field in a trace session.

## -struct-fields

### -field FieldName

The name of the field to filter in package manifest.

### -field CompareOp

The payload operator to use for the comparison.

This member can be one of the values for the [**PAYLOAD_OPERATOR**](ne-tdh-payload_operator.md) enumeration defined in the *Tdh.h* header file. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PAYLOADFIELD_EQ"></a><a id="payloadfield_eq"></a><dl>
<dt><b>PAYLOADFIELD_EQ</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The value of the <b>FieldName</b> parameter is equal to the numeric value of the string in the <b>Value</b> member. 

This operator is for comparing integers and requires one value in the <b>Value</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="PAYLOADFIELD_NE"></a><a id="payloadfield_ne"></a><dl>
<dt><b>PAYLOADFIELD_NE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The value of the <b>FieldName</b> parameter is not equal to the numeric value of the string in the <b>Value</b> member. 

This operator is for comparing integers and requires one value in the <b>Value</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="PAYLOADFIELD_LE"></a><a id="payloadfield_le"></a><dl>
<dt><b>PAYLOADFIELD_LE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The value of the <b>FieldName</b> parameter is less than or equal to the numeric value of the string in the <b>Value</b> member. 

This operator is for comparing integers and requires one value in the <b>Value</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="PAYLOADFIELD_GT"></a><a id="payloadfield_gt"></a><dl>
<dt><b>PAYLOADFIELD_GT</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The value of the <b>FieldName</b> parameter is greater than the numeric value of the string in the <b>Value</b> member. 

This operator is for comparing integers and requires one value in the <b>Value</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="PAYLOADFIELD_LT"></a><a id="payloadfield_lt"></a><dl>
<dt><b>PAYLOADFIELD_LT</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The value of the <b>FieldName</b> parameter is less than the numeric value of the string in the  <b>Value</b> member. 

This operator is for comparing integers and requires one value in the <b>Value</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="PAYLOADFIELD_GE"></a><a id="payloadfield_ge"></a><dl>
<dt><b>PAYLOADFIELD_GE</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The value of the <b>FieldName</b> parameter is greater than or equal to the numeric value of the string in the <b>Value</b> member. 

This operator is for comparing integers and requires one value in the <b>Value</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="PAYLOADFIELD_BETWEEN"></a><a id="payloadfield_between"></a><dl>
<dt><b>PAYLOADFIELD_BETWEEN</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The value of the <b>FieldName</b> parameter is between the two numeric values in the string in the <b>Value</b> member. The  <b>PAYLOADFIELD_BETWEEN</b> operator uses a closed interval (LowerBound &lt;= FieldValue &lt;= UpperBound).

This operator is for comparing integers and requires two values in the <b>Value</b> member. The two values should be separated by a comma character (',').

</td>
</tr>
<tr>
<td width="40%"><a id="PAYLOADFIELD_NOTBETWEEN"></a><a id="payloadfield_notbetween"></a><dl>
<dt><b>PAYLOADFIELD_NOTBETWEEN</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
The value of the <b>FieldName</b> parameter is not between the two numeric values in the string in the <b>Value</b> member. 

This operator is for comparing integers and requires two values in the <b>Value</b> member. The two values should be separated by a comma character (',').

</td>
</tr>
<tr>
<td width="40%"><a id="PAYLOADFIELD_MODULO"></a><a id="payloadfield_modulo"></a><dl>
<dt><b>PAYLOADFIELD_MODULO</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The value of the <b>FieldName</b> parameter is the modulo of the  numeric value in the string in the <b>Value</b> member. The operator can be used for periodic sampling. 

This operator is for comparing integers and requires one value in the <b>Value</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="PAYLOADFIELD_CONTAINS"></a><a id="payloadfield_contains"></a><dl>
<dt><b>PAYLOADFIELD_CONTAINS</b></dt>
<dt>20</dt>
</dl>
</td>
<td width="60%">
The value of the <b>FieldName</b> parameter contains the substring value in the <b>Value</b> member. String comparisons are case insensitive.

This operator is for comparing strings and requires one value in the <b>Value</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="PAYLOADFIELD_DOESNTCONTAIN"></a><a id="payloadfield_doesntcontain"></a><dl>
<dt><b>PAYLOADFIELD_DOESNTCONTAIN</b></dt>
<dt>21</dt>
</dl>
</td>
<td width="60%">
The value of the <b>FieldName</b> parameter does not contain the substring in the <b>Value</b> member. String comparisons are case insensitive.

This operator is for comparing strings and requires one value in the <b>Value</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="PAYLOADFIELD_IS"></a><a id="payloadfield_is"></a><dl>
<dt><b>PAYLOADFIELD_IS</b></dt>
<dt>30</dt>
</dl>
</td>
<td width="60%">
The value of the <b>FieldName</b> parameter is identical to the value of the string in the <b>Value</b> member. String comparisons are case insensitive.

This operator is for comparing strings or other non-integer values and requires one value in the <b>Value</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="PAYLOADFIELD_ISNOT"></a><a id="payloadfield_isnot"></a><dl>
<dt><b>PAYLOADFIELD_ISNOT</b></dt>
<dt>31</dt>
</dl>
</td>
<td width="60%">
The value of the <b>FieldName</b> parameter is not identical to the value of the string in the <b>Value</b> member. String comparisons are case insensitive.

This operator is for comparing strings or other non-integer values and requires one value in the <b>Value</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="PAYLOADFIELD_INVALID"></a><a id="payloadfield_invalid"></a><dl>
<dt><b>PAYLOADFIELD_INVALID</b></dt>
<dt>32</dt>
</dl>
</td>
<td width="60%">
A value of the payload operator that is not valid.

</td>
</tr>
</table>

### -field Value

The string that contains one or values to compare depending on the <b>CompareOp</b> member.

## -remarks

On Windows 8.1,Windows Server 2012 R2, and later, event payload filters can be used by the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function and the <a href="/windows/desktop/ETW/enable-trace-parameters">ENABLE_TRACE_PARAMETERS</a> and <a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a> structures to filter on the specific content of the event in a logger session. 

The <b>PAYLOAD_FILTER_PREDICATE</b> structure is used with the <a href="/windows/desktop/api/tdh/nf-tdh-tdhcreatepayloadfilter">TdhCreatePayloadFilter</a> function to create a single payload filter for a single payload to be used with the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function.  A single payload filter can also be aggregated with other single payload filters using the <a href="/windows/desktop/api/tdh/nf-tdh-tdhaggregatepayloadfilters">TdhAggregatePayloadFilters</a> function.

Each field has a type specified in the provider manifest that can be used in the <b>Fieldname</b> member of the <b>PAYLOAD_FILTER_PREDICATE</b> structure to filter on that field.  

The <b>CompareOp</b> member specifies that operator  to use for payload filtering. Payload filtering supports filtering on a string (including a <b>GUID</b>) and integers (including <b>TDH_INTYPE_FILETIME</b>).  Filtering on floating-point numbers, a binary blob (including <b>TDH_INTYPE_POINTER</b>), and structured data (<b>SID</b> and <b>SYSTEMTIME</b>) are not supported.

The <b>Value</b> member contains a string of the value or values to compare with the value of the <b>Fieldname</b> member. The <b>Value</b> member is converted from a string to the type of the <b>Fieldname</b> member as specified in the manifest. 

All string comparisons are case-insensitive.  The string in the <b>Value</b> member is UNICODE, but it will be converted to ANSI if the type specified in the manifest is ANSI.  

A <b>Fieldname</b> member that contains a <b>GUID</b> can only be compared when the <b>CompareOp</b> member contains either the  <b>PAYLOADFIELD_IS</b> or <b>PAYLOADFIELD_ISNOT</b> for the payload operator. The string that represents a <b>GUID</b> in the <b>Value</b> member must contain the curly brackets ({00000000-0000-0000-0000-000000000000}, for example).


#### Examples

For an example that uses 
the <b>PAYLOAD_FILTER_PREDICATE</b> structure and the <a href="/windows/desktop/api/tdh/nf-tdh-tdhcreatepayloadfilter">TdhCreatePayloadFilter</a> function to create payload filters to use in filtering on specific conditions in a logger session, see 
the example for the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function.

<div class="code"></div>

## -see-also
<a href="/windows/desktop/ETW/enable-trace-parameters">ENABLE_TRACE_PARAMETERS</a>



<a href="/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a>



<a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a>



<a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhaggregatepayloadfilters">TdhAggregatePayloadFilters</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhcreatepayloadfilter">TdhCreatePayloadFilter</a>
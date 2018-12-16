---
UID: NF:winsnmp.SnmpOidCompare
title: SnmpOidCompare function
author: windows-sdk-content
description: The WinSNMP SnmpOidCompare function lexicographically compares two SNMP object identifiers, up to the length specified by the maxlen parameter.
old-location: snmp\snmpoidcompare.htm
tech.root: SNMP
ms.assetid: aa13abb3-c16d-4b12-a3b8-9c3c727199e0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Equal to 0, Greater than 0, Less than 0, SnmpOidCompare, SnmpOidCompare function [SNMP], _snmp_snmpoidcompare, snmp.snmpoidcompare, winsnmp/SnmpOidCompare
ms.topic: function
req.header: winsnmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsnmp32.dll
api_name:
 - SnmpOidCompare
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpOidCompare function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpOidCompare</b> function lexicographically compares two SNMP object identifiers, up to the length specified by the <i>maxlen</i> parameter.


## -parameters




### -param xOID [in]

Pointer to the first 
<a href="https://msdn.microsoft.com/en-us/library/Aa377996(v=VS.85).aspx">smiOID</a> object identifier to compare. The length of the object identifier can be zero.


### -param yOID [in]

Pointer to the second 
<a href="https://msdn.microsoft.com/en-us/library/Aa377996(v=VS.85).aspx">smiOID</a> object identifier to compare. The length of the object identifier can be zero.


### -param maxlen [in]

If not equal to zero, specifies the number of subidentifiers to compare. This parameter must be less than MAXOBJIDSIZE: 128 subidentifiers, the maximum number of components in an object identifier. For additional information, see the following Remarks section.


### -param result [out]

Pointer to an integer variable to receive the result of the comparison. The variable can receive one of the following results. 



<table>
<tr>
<th>Result</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Greater_than_0"></a><a id="greater_than_0"></a><a id="GREATER_THAN_0"></a><dl>
<dt><b>Greater than 0</b></dt>
</dl>
</td>
<td width="60%">
<i>xOID</i> is greater than <i>yOID</i>

</td>
</tr>
<tr>
<td width="40%"><a id="Equal_to_0"></a><a id="equal_to_0"></a><a id="EQUAL_TO_0"></a><dl>
<dt><b>Equal to 0</b></dt>
</dl>
</td>
<td width="60%">
<i>xOID</i> equals <i>yOID</i>

</td>
</tr>
<tr>
<td width="40%"><a id="Less_than_0"></a><a id="less_than_0"></a><a id="LESS_THAN_0"></a><dl>
<dt><b>Less than 0</b></dt>
</dl>
</td>
<td width="60%">
<i>xOID</i> is less than <i>yOID</i>

</td>
</tr>
</table>
 

For additional comparison conditions, see the following Remarks section.


## -returns



If the function succeeds, the return value is SNMPAPI_SUCCESS.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="https://msdn.microsoft.com/0cfb2bc3-cfa5-4806-9dcf-119541463e7b">SnmpGetLastError</a> specifying a <b>NULL</b> value in its <i>session</i> parameter. The 
<b>SnmpGetLastError</b> function can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The 
<a href="https://msdn.microsoft.com/7b8a4a1e-871f-424b-8bcb-c0b3bfaae9ce">SnmpStartup</a> function did not complete successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_ALLOC_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_OID_INVALID</b></dt>
</dl>
</td>
<td width="60%">
One or both of the <i>xOID</i> and <i>yOID</i> parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_SIZE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>maxlen</i> parameter is invalid. The parameter size is greater than MAXOBJIDSIZE.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_OTHER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An unknown or undefined error occurred.

</td>
</tr>
</table>
 




## -remarks



A WinSNMP application can call the 
<b>SnmpOidCompare</b> function to determine whether two object identifiers have common prefixes.

If the <i>maxlen</i> parameter is not equal to zero, and not greater than MAXOBJIDSIZE, the value of <i>maxlen</i> sets the upper limit for the number of subidentifiers to compare. The maximum number of subidentifiers that the 
<b>SnmpOidCompare</b> function compares defaults to whichever is the smallest number—the <i>maxlen</i> parameter, or the <b>len</b> member of one of the 
<a href="https://msdn.microsoft.com/en-us/library/Aa377996(v=VS.85).aspx">smiOID</a> structures pointed to by the <i>xOID</i> and <i>yOID</i> parameters.

If the <i>maxlen</i> parameter is equal to zero, the maximum number of subidentifiers that the 
<b>SnmpOidCompare</b> function compares defaults to the number that is the smaller of the <b>len</b> members of the two 
<a href="https://msdn.microsoft.com/en-us/library/Aa377996(v=VS.85).aspx">smiOID</a> structures.

The value of the <i>result</i> parameter will indicate that <i>xOID</i> equals <i>yOID</i> if the two 
<a href="https://msdn.microsoft.com/en-us/library/Aa377996(v=VS.85).aspx">smiOID</a> structures are lexicographically equal and one of the following occurs:

<ul>
<li><b>SnmpOidCompare</b> compares a <i>maxlen</i> number of subidentifiers.</li>
<li><b>SnmpOidCompare</b> compares the maximum number of subidentifiers, and the <b>len</b> members of both 
<a href="https://msdn.microsoft.com/en-us/library/Aa377996(v=VS.85).aspx">smiOID</a> structures are equal, but less than the <i>maxlen</i> parameter.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377996(v=VS.85).aspx">smiOID</a>
 

 


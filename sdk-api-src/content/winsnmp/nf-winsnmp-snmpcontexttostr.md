---
UID: NF:winsnmp.SnmpContextToStr
title: SnmpContextToStr function (winsnmp.h)
description: The WinSNMP SnmpContextToStr function returns a string that identifies an SNMP context, which is a set of managed object resources. The function returns the string in an smiOCTETS structure.
helpviewer_keywords: ["SnmpContextToStr","SnmpContextToStr function [SNMP]","_snmp_snmpcontexttostr","snmp.snmpcontexttostr","winsnmp/SnmpContextToStr"]
old-location: snmp\snmpcontexttostr.htm
tech.root: SNMP
ms.assetid: d82c352d-8685-4276-b58c-ce89557f074a
ms.date: 12/05/2018
ms.keywords: SnmpContextToStr, SnmpContextToStr function [SNMP], _snmp_snmpcontexttostr, snmp.snmpcontexttostr, winsnmp/SnmpContextToStr
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpContextToStr
 - winsnmp/SnmpContextToStr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsnmp32.dll
api_name:
 - SnmpContextToStr
---

# SnmpContextToStr function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpContextToStr</b> function returns a string that identifies an SNMP context, which is a set of managed object resources. The function returns the string in an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a> structure.

## -parameters

### -param context [in]

Handle to the SNMP context of interest.

### -param string [out]

Pointer to an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a> structure to receive the string that identifies the context of interest. The string can have a null-terminating byte.

## -returns

If the function succeeds, the return value is SNMPAPI_SUCCESS.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a>. The 
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
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> function did not complete successfully.

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
<dt><b>SNMPAPI_CONTEXT_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>context</i> parameter is invalid.

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

The current setting of the entity and context translation mode determines the type of output string 
<b>SnmpContextToStr</b> returns. For additional information, see 
<a href="/windows/desktop/SNMP/setting-the-entity-and-context-translation-mode">Setting the Entity and Context Translation Mode</a>.

The WinSNMP application must provide the address of a valid 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a> structure for the <i>string</i> parameter. If the 
<b>SnmpContextToStr</b> function completes successfully, the Microsoft WinSNMP implementation initializes the <b>len</b> and <b>ptr</b> members of the structure. The WinSNMP application must call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a> function to enable the implementation to free the resources for these members.

When the entity and context translation mode is SNMPAPI_TRANSLATED, and the entry exists in the implementation's database, the implementation returns the associated user-friendly name of the context. If an entry does not exist for the context name, 
<b>SnmpContextToStr</b> returns the SNMP community string.

When the entity and context translation mode is SNMPAPI_UNTRANSLATED_V1 or SNMPAPI_UNTRANSLATED_V2, the implementation also returns the SNMP community string.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a>
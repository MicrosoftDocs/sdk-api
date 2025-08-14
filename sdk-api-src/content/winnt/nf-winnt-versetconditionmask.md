---
UID: NF:winnt.VerSetConditionMask
title: VerSetConditionMask function (winnt.h)
description: Sets the bits of a 64-bit value to indicate the comparison operator to use for a specified operating system version attribute. This function is used to build the dwlConditionMask parameter of the VerifyVersionInfo function.
helpviewer_keywords: ["VER_AND","VER_BUILDNUMBER","VER_EQUAL","VER_GREATER","VER_GREATER_EQUAL","VER_LESS","VER_LESS_EQUAL","VER_MAJORVERSION","VER_MINORVERSION","VER_OR","VER_PLATFORMID","VER_PRODUCT_TYPE","VER_SERVICEPACKMAJOR","VER_SERVICEPACKMINOR","VER_SUITENAME","VerSetConditionMask","VerSetConditionMask function","_win32_versetconditionmask","base.versetconditionmask","winnt/VerSetConditionMask"]
old-location: base\versetconditionmask.htm
tech.root: winprog
ms.assetid: 5ee18447-e55f-4d79-9d21-be7a619ea647
ms.date: 12/05/2018
ms.keywords: VER_AND, VER_BUILDNUMBER, VER_EQUAL, VER_GREATER, VER_GREATER_EQUAL, VER_LESS, VER_LESS_EQUAL, VER_MAJORVERSION, VER_MINORVERSION, VER_OR, VER_PLATFORMID, VER_PRODUCT_TYPE, VER_SERVICEPACKMAJOR, VER_SERVICEPACKMINOR, VER_SUITENAME, VerSetConditionMask, VerSetConditionMask function, _win32_versetconditionmask, base.versetconditionmask, winnt/VerSetConditionMask
req.header: winnt.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VerSetConditionMask
 - winnt/VerSetConditionMask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-sysinfo-l1-2-7.dll
 - api-ms-win-core-sysinfo-l1-2-6.dll
 - api-ms-win-core-sysinfo-l1-2-5.dll
 - api-ms-win-core-sysinfo-l1-2-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
 - Ntdll.dll
api_name:
 - VerSetConditionMask
---

# VerSetConditionMask function


## -description

Sets the bits of a 64-bit value to indicate the comparison operator to use for a specified operating system version attribute. This function is used to build the <i>dwlConditionMask</i> parameter of the 
<a href="/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa">VerifyVersionInfo</a> function.

## -parameters

### -param ConditionMask [in]

A value to be passed as the <i>dwlConditionMask</i> parameter of the 
<a href="/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa">VerifyVersionInfo</a> function. The function stores the comparison information in the bits of this variable. 




Before the first call to <b>VerSetCondition</b>, initialize this variable to zero. For subsequent calls, pass in the variable used in the previous call.

### -param TypeMask [in]

A mask that indicates the member of the 
<a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">OSVERSIONINFOEX</a> structure whose comparison operator is being set. This value corresponds to one of the bits specified in the <i>dwTypeMask</i> parameter for the 
<a href="/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa">VerifyVersionInfo</a> function. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VER_BUILDNUMBER"></a><a id="ver_buildnumber"></a><dl>
<dt><b>VER_BUILDNUMBER</b></dt>
<dt>0x0000004</dt>
</dl>
</td>
<td width="60%">
dwBuildNumber

</td>
</tr>
<tr>
<td width="40%"><a id="VER_MAJORVERSION"></a><a id="ver_majorversion"></a><dl>
<dt><b>VER_MAJORVERSION</b></dt>
<dt>0x0000002</dt>
</dl>
</td>
<td width="60%">
dwMajorVersion

</td>
</tr>
<tr>
<td width="40%"><a id="VER_MINORVERSION"></a><a id="ver_minorversion"></a><dl>
<dt><b>VER_MINORVERSION</b></dt>
<dt>0x0000001</dt>
</dl>
</td>
<td width="60%">
dwMinorVersion

</td>
</tr>
<tr>
<td width="40%"><a id="VER_PLATFORMID"></a><a id="ver_platformid"></a><dl>
<dt><b>VER_PLATFORMID</b></dt>
<dt>0x0000008</dt>
</dl>
</td>
<td width="60%">
dwPlatformId

</td>
</tr>
<tr>
<td width="40%"><a id="VER_PRODUCT_TYPE"></a><a id="ver_product_type"></a><dl>
<dt><b>VER_PRODUCT_TYPE</b></dt>
<dt>0x0000080</dt>
</dl>
</td>
<td width="60%">
wProductType

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SERVICEPACKMAJOR"></a><a id="ver_servicepackmajor"></a><dl>
<dt><b>VER_SERVICEPACKMAJOR</b></dt>
<dt>0x0000020</dt>
</dl>
</td>
<td width="60%">
wServicePackMajor

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SERVICEPACKMINOR"></a><a id="ver_servicepackminor"></a><dl>
<dt><b>VER_SERVICEPACKMINOR</b></dt>
<dt>0x0000010</dt>
</dl>
</td>
<td width="60%">
wServicePackMinor

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITENAME"></a><a id="ver_suitename"></a><dl>
<dt><b>VER_SUITENAME</b></dt>
<dt>0x0000040</dt>
</dl>
</td>
<td width="60%">
wSuiteMask

</td>
</tr>
</table>

### -param Condition [in]

The operator to be used for the comparison. The 
<a href="/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa">VerifyVersionInfo</a> function uses this operator to compare a specified attribute value to the corresponding value for the currently running system. 




For all values of <i>dwTypeBitMask</i> other than VER_SUITENAME, this parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VER_EQUAL"></a><a id="ver_equal"></a><dl>
<dt><b>VER_EQUAL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The current value must be equal to the specified value.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_GREATER"></a><a id="ver_greater"></a><dl>
<dt><b>VER_GREATER</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The current value must be greater than the specified value.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_GREATER_EQUAL"></a><a id="ver_greater_equal"></a><dl>
<dt><b>VER_GREATER_EQUAL</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The current value must be greater than or equal to the specified value.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_LESS"></a><a id="ver_less"></a><dl>
<dt><b>VER_LESS</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The current value must be less than the specified value.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_LESS_EQUAL"></a><a id="ver_less_equal"></a><dl>
<dt><b>VER_LESS_EQUAL</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The current value must be less than or equal to the specified value.

</td>
</tr>
</table>
 

If <i>dwTypeBitMask</i> is VER_SUITENAME, this parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VER_AND"></a><a id="ver_and"></a><dl>
<dt><b>VER_AND</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
All product suites specified in the <b>wSuiteMask</b> member must be present in the current system.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_OR"></a><a id="ver_or"></a><dl>
<dt><b>VER_OR</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
At least one of the specified product suites must be present in the current system.

</td>
</tr>
</table>

## -returns

The function returns the condition mask value.

## -remarks

Call this function once for each bit set in the <i>dwTypeMask</i> parameter of the 
<a href="/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa">VerifyVersionInfo</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/SysInfo/verifying-the-system-version">Verifying the System Version</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">OSVERSIONINFOEX</a>



<a href="/windows/desktop/SysInfo/operating-system-version">Operating System Version</a>



<a href="/windows/desktop/SysInfo/system-information-functions">System Information Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa">VerifyVersionInfo</a>
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

# VER_SET_CONDITION macro


## -description


Sets the bits of a 64-bit value to indicate the comparison operator to use for a specified operating system version attribute. This macro is used to build the <i>dwlConditionMask</i> parameter of the 
<a href="https://msdn.microsoft.com/791bc6bf-f486-4110-b6ea-30a0935040b2">VerifyVersionInfo</a> function.


## -parameters




### -param _m_

TBD


### -param _t_

TBD


### -param _c_

TBD






#### - dwConditionMask

The operator to use for the comparison. The 
<a href="https://msdn.microsoft.com/791bc6bf-f486-4110-b6ea-30a0935040b2">VerifyVersionInfo</a> function uses this operator to compare a specified attribute value to the corresponding value for the currently running system. 




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
 


#### - dwTypeBitMask

A mask that indicates the member of the 
<a href="https://msdn.microsoft.com/4ab07a72-404d-459b-b061-b3b06b5db37e">OSVERSIONINFOEX</a> structure whose comparison type is being set. This value corresponds to one of the bits specified in the <i>dwTypeMask</i> parameter for the 
<a href="https://msdn.microsoft.com/791bc6bf-f486-4110-b6ea-30a0935040b2">VerifyVersionInfo</a> function. This parameter can be one of the following values.

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
 


#### - dwlConditionMask

A variable to be passed as the <i>dwlConditionMask</i> parameter of the 
<a href="https://msdn.microsoft.com/791bc6bf-f486-4110-b6ea-30a0935040b2">VerifyVersionInfo</a> function. The macro stores the comparison information in the bits of this variable. 




Before the first call to 
<b>VER_SET_CONDITION</b>, initialize this variable to zero. For subsequent calls to 
<b>VER_SET_CONDITION</b>, pass in the variable used in the previous call.


## -remarks



Call this macro once for each bit set in the <i>dwTypeMask</i> parameter of the 
<a href="https://msdn.microsoft.com/791bc6bf-f486-4110-b6ea-30a0935040b2">VerifyVersionInfo</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/f39c35ae-9be5-4a03-9079-6fcc63387f6b">Verifying the System Version</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4ab07a72-404d-459b-b061-b3b06b5db37e">OSVERSIONINFOEX</a>



<a href="https://msdn.microsoft.com/791bc6bf-f486-4110-b6ea-30a0935040b2">VerifyVersionInfo</a>
 

 


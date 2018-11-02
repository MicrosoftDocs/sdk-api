---
UID: NF:winbase.VerifyVersionInfoA
title: VerifyVersionInfoA function
author: windows-sdk-content
description: Compares a set of operating system version requirements to the corresponding values for the currently running version of the system.
old-location: base\verifyversioninfo.htm
tech.root: sysinfo
ms.assetid: 791bc6bf-f486-4110-b6ea-30a0935040b2
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: VER_BUILDNUMBER, VER_MAJORVERSION, VER_MINORVERSION, VER_PLATFORMID, VER_PRODUCT_TYPE, VER_SERVICEPACKMAJOR, VER_SERVICEPACKMINOR, VER_SUITENAME, VerifyVersionInfo, VerifyVersionInfo function, VerifyVersionInfoA, VerifyVersionInfoW, _win32_verifyversioninfo, base.verifyversioninfo, winbase/VerifyVersionInfo, winbase/VerifyVersionInfoA, winbase/VerifyVersionInfoW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: VerifyVersionInfoW (Unicode) and VerifyVersionInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - VerifyVersionInfo
 - VerifyVersionInfoA
 - VerifyVersionInfoW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VerifyVersionInfoA function


## -description


Compares a set of operating system version requirements to the corresponding values for the currently running version of the system.This function is subject to manifest-based behavior.  For more information, see the Remarks section.


## -parameters




### -param lpVersionInformation [in]

A pointer to an 
<a href="https://msdn.microsoft.com/4ab07a72-404d-459b-b061-b3b06b5db37e">OSVERSIONINFOEX</a> structure containing the operating system version requirements to compare. The <i>dwTypeMask</i> parameter indicates the members of this structure that contain information to compare. 




You must set the <b>dwOSVersionInfoSize</b> member of this structure to <code>sizeof(OSVERSIONINFOEX)</code>. You must also specify valid data for the members indicated by <i>dwTypeMask</i>. The function ignores structure members for which the corresponding <i>dwTypeMask</i> bit is not set.


### -param dwTypeMask [in]

A mask that indicates the members of the 
<a href="https://msdn.microsoft.com/4ab07a72-404d-459b-b061-b3b06b5db37e">OSVERSIONINFOEX</a> structure to be tested. This parameter can be one or more of the following values.

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
<b>dwBuildNumber</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VER_MAJORVERSION"></a><a id="ver_majorversion"></a><dl>
<dt><b>VER_MAJORVERSION</b></dt>
<dt>0x0000002</dt>
</dl>
</td>
<td width="60%">
<b>dwMajorVersion</b>

If you are testing the major version, you must also test the minor version and the service pack major and minor versions.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_MINORVERSION"></a><a id="ver_minorversion"></a><dl>
<dt><b>VER_MINORVERSION</b></dt>
<dt>0x0000001</dt>
</dl>
</td>
<td width="60%">
<b>dwMinorVersion</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VER_PLATFORMID"></a><a id="ver_platformid"></a><dl>
<dt><b>VER_PLATFORMID</b></dt>
<dt>0x0000008</dt>
</dl>
</td>
<td width="60%">
<b>dwPlatformId</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SERVICEPACKMAJOR"></a><a id="ver_servicepackmajor"></a><dl>
<dt><b>VER_SERVICEPACKMAJOR</b></dt>
<dt>0x0000020</dt>
</dl>
</td>
<td width="60%">
<b>wServicePackMajor</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SERVICEPACKMINOR"></a><a id="ver_servicepackminor"></a><dl>
<dt><b>VER_SERVICEPACKMINOR</b></dt>
<dt>0x0000010</dt>
</dl>
</td>
<td width="60%">
<b>wServicePackMinor</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VER_SUITENAME"></a><a id="ver_suitename"></a><dl>
<dt><b>VER_SUITENAME</b></dt>
<dt>0x0000040</dt>
</dl>
</td>
<td width="60%">
<b>wSuiteMask</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VER_PRODUCT_TYPE"></a><a id="ver_product_type"></a><dl>
<dt><b>VER_PRODUCT_TYPE</b></dt>
<dt>0x0000080</dt>
</dl>
</td>
<td width="60%">
<b>wProductType</b>

</td>
</tr>
</table>
 


### -param dwlConditionMask [in]

The type of comparison to be used for each <b>lpVersionInfo</b> member being compared. To build this value, call the 
<a href="https://msdn.microsoft.com/5ee18447-e55f-4d79-9d21-be7a619ea647">VerSetConditionMask</a> function or the 
<a href="https://msdn.microsoft.com/c93be952-41a8-48c4-b24f-996bf9237727">VER_SET_CONDITION</a> macro once for each 
<a href="https://msdn.microsoft.com/4ab07a72-404d-459b-b061-b3b06b5db37e">OSVERSIONINFOEX</a> member being compared.


## -returns



If the currently running operating system satisfies the specified requirements, the return value is a nonzero value.

If the current system does not satisfy the requirements, the return value is zero and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_OLD_WIN_VERSION.

If the function fails, the return value is zero and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns an error code other than ERROR_OLD_WIN_VERSION.




## -remarks



The 
<b>VerifyVersionInfo</b> function retrieves version information about the currently running operating system and compares it to the valid members of the <b>lpVersionInfo</b> structure. This enables you to easily determine the presence of a required set of operating system version conditions. It is preferable to use 
<b>VerifyVersionInfo</b> rather than calling the 
<a href="https://msdn.microsoft.com/8e3ab4d6-bacd-4bc5-b8f6-dd49289354de">GetVersionEx</a> function to perform your own comparisons.

Typically, 
<b>VerifyVersionInfo</b> returns a nonzero value only if all specified tests succeed. However, major, minor, and service pack versions are tested in a hierarchical manner because the operating system version is a combination of these values. If a condition exists for the major version, it supersedes the conditions specified for minor version and service pack version. (You cannot test for major version greater than 5 and minor version less than or equal to 1. If you specify such a test, the function will change the request to test for a minor version greater than 1 because it is performing a greater than operation on the major version.)

The function tests these values in this order: major version, minor version, and service pack version. The function continues testing values while they are equal, and stops when one of the values does not meet the specified condition. For example, if you test for a system greater than or equal to version 5.1 service pack 1, the test succeeds if the current version is 6.0. (The major version is greater than the specified version, so the testing stops.) In the same way, if you test for a system greater than or equal to version 5.1 service pack 1, the test succeeds if the current version is 5.2. (The minor version is greater than the specified versions, so the testing stops.) However, if you test for a system greater than or equal to version 5.1 service pack 1, the test fails if the current version is 5.0 service pack 2. (The minor version is not greater than the specified version, so the testing stops.)

To verify a range of system versions, you must call 
<b>VerifyVersionInfo</b> twice. For example, to verify that the system version is greater than 5.0 but less than or equal to 5.1, first call 
<b>VerifyVersionInfo</b> to test that the major version is 5 and the minor version is greater than 0, then call 
<b>VerifyVersionInfo</b> again to test that the major version is 5 and the minor version is less than or equal to 1.

Identifying the current operating system is usually not the best way to determine whether a particular operating system feature is present. This is because the operating system may have had new features added in a redistributable DLL. Rather than using 
<a href="https://msdn.microsoft.com/8e3ab4d6-bacd-4bc5-b8f6-dd49289354de">GetVersionEx</a> to determine the operating system platform or version number, test for the presence of the feature itself. For more information, see 
<a href="https://msdn.microsoft.com/1a70b1d9-ed66-4201-9921-4e26e4001020">Operating System Version</a>.

To verify whether the current operating system is either the Media Center or Tablet PC version of Windows, call <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a>.

<b>Windows 10:  </b><b>VerifyVersionInfo</b> returns false when called by applications that do not have a compatibility manifest for Windows 8.1 or Windows 10 if the <i>lpVersionInfo</i> parameter is set so that it specifies Windows 8.1 or Windows 10, even when the current operating system version is Windows 8.1 or Windows 10. Specifically, <b>VerifyVersionInfo</b> has the following behavior:<ul>
<li>If  the application has no manifest, <b>VerifyVersionInfo</b> behaves as if the operation system version is Windows 8 (6.2).</li>
<li>If  the application has a manifest that contains the GUID that corresponds to Windows 8.1, <b>VerifyVersionInfo</b> behaves as if the operation system version is Windows 8.1 (6.3).</li>
<li>If  the application has a manifest that contains the GUID that corresponds to Windows 10, <b>VerifyVersionInfo</b> behaves as if the operation system version is Windows 10 (10.0).</li>
</ul>
The <a href="https://msdn.microsoft.com/2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34">Version Helper functions</a> use the <b>VerifyVersionInfo</b> function, so the behavior <a href="https://msdn.microsoft.com/E391B568-5E43-42C7-B186-8CA524331FFE">IsWindows8Point1OrGreater</a> and <a href="https://msdn.microsoft.com/1F7AE6CA-3E2B-4DF1-A047-58AB9A0B1DA4">IsWindows10OrGreater</a> are similarly affected by the presence and content of the manifest.

To manifest your applications for Windows 8.1 or Windows 10, see <a href="https://msdn.microsoft.com/E7A1A16A-95B3-4B45-81AD-A19E33F15AE4">Targeting your application for Windows</a>.




#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/f39c35ae-9be5-4a03-9079-6fcc63387f6b">Verifying the System Version</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8e3ab4d6-bacd-4bc5-b8f6-dd49289354de">GetVersionEx</a>



<a href="https://msdn.microsoft.com/4ab07a72-404d-459b-b061-b3b06b5db37e">OSVERSIONINFOEX</a>



<a href="https://msdn.microsoft.com/1a70b1d9-ed66-4201-9921-4e26e4001020">Operating System Version</a>



<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System Information Functions</a>



<a href="https://msdn.microsoft.com/c93be952-41a8-48c4-b24f-996bf9237727">VER_SET_CONDITION</a>



<a href="https://msdn.microsoft.com/5ee18447-e55f-4d79-9d21-be7a619ea647">VerSetConditionMask</a>
 

 


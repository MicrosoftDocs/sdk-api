---
UID: NF:shlwapi.IsOS
title: IsOS function (shlwapi.h)
description: Checks for specified operating systems and operating system features.
helpviewer_keywords: ["IsOS","IsOS function [Windows Shell]","_win32_IsOS","shell.IsOS","shlwapi/IsOS"]
old-location: shell\IsOS.htm
tech.root: shell
ms.assetid: 827a76bc-3581-4f1c-8095-8e2fd30dfdbc
ms.date: 12/05/2018
ms.keywords: IsOS, IsOS function [Windows Shell], _win32_IsOS, shell.IsOS, shlwapi/IsOS
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
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
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsOS
 - shlwapi/IsOS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-shlwapi-l2-1-0.dll
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - ShCore.dll
 - API-MS-Win-ShCore-SysInfo-l1-1-0.dll
api_name:
 - IsOS
---

# IsOS function


## -description

Checks for specified operating systems and operating system features.

## -parameters

### -param dwOS [in]

Type: <b>DWORD</b>

A value that specifies which operating system or operating system feature to check for. One of the following values (you cannot combine values).
    
                        

<table class="clsStd">
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>OS_WINDOWS</td>
<td>0</td>
<td>The program is running on one of the following versions of Windows:
    
                                    <ul>
<li>Windows 95</li>
<li>Windows 98</li>
<li>Windows Me</li>
</ul>
Equivalent to <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_PLATFORM_WIN32_WINDOWS</a>. Note that none of those systems are supported at this time. <b>OS_WINDOWS</b> returns <b>FALSE</b> on all supported systems.

</td>
</tr>
<tr>
<td>OS_NT</td>
<td>1</td>
<td>Always returns <b>TRUE</b>.</td>
</tr>
<tr>
<td>OS_WIN95ORGREATER</td>
<td>2</td>
<td>Always returns <b>FALSE</b>.</td>
</tr>
<tr>
<td>OS_NT4ORGREATER</td>
<td>3</td>
<td>Always returns <b>FALSE</b>.</td>
</tr>
<tr>
<td>OS_WIN98ORGREATER</td>
<td>5</td>
<td>Always returns <b>FALSE</b>.</td>
</tr>
<tr>
<td>OS_WIN98_GOLD</td>
<td>6</td>
<td>Always returns <b>FALSE</b>.</td>
</tr>
<tr>
<td>OS_WIN2000ORGREATER</td>
<td>7</td>
<td>The program is running on Windows 2000 or one of its successors.</td>
</tr>
<tr>
<td>OS_WIN2000PRO</td>
<td>8</td>
<td>Do not use; use OS_PROFESSIONAL.</td>
</tr>
<tr>
<td>OS_WIN2000SERVER</td>
<td>9</td>
<td>Do not use; use OS_SERVER.</td>
</tr>
<tr>
<td>OS_WIN2000ADVSERVER</td>
<td>10</td>
<td>Do not use; use OS_ADVSERVER.</td>
</tr>
<tr>
<td>OS_WIN2000DATACENTER</td>
<td>11</td>
<td>Do not use; use OS_DATACENTER.</td>
</tr>
<tr>
<td>OS_WIN2000TERMINAL</td>
<td>12</td>
<td>The program is running on Windows 2000 Terminal Server in either Remote Administration mode or Application Server mode, or Windows Server 2003  (or one of its successors) in Terminal Server mode or Remote Desktop for Administration mode. Consider using a more specific value such as OS_TERMINALSERVER, OS_TERMINALREMOTEADMIN, or  OS_PERSONALTERMINALSERVER.</td>
</tr>
<tr>
<td>OS_EMBEDDED</td>
<td>13</td>
<td>The program is running on Windows Embedded, any version. Equivalent to <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_SUITE_EMBEDDEDNT</a>.</td>
</tr>
<tr>
<td>OS_TERMINALCLIENT</td>
<td>14</td>
<td>The program is running as a Terminal Server client. Equivalent to <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>(SM_REMOTESESSION).</td>
</tr>
<tr>
<td>OS_TERMINALREMOTEADMIN</td>
<td>15</td>
<td>The program is running on Windows 2000 Terminal Server in the Remote Administration mode or Windows Server 2003 (or one of its successors) in the Remote Desktop for Administration mode (these are the default installation modes). This is equivalent to <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_SUITE_TERMINAL</a> &amp;&amp; <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_SUITE_SINGLEUSERTS</a>.</td>
</tr>
<tr>
<td>OS_WIN95_GOLD</td>
<td>16</td>
<td>Always returns <b>FALSE</b>.</td>
</tr>
<tr>
<td>OS_MEORGREATER</td>
<td>17</td>
<td>Always returns <b>FALSE</b>.</td>
</tr>
<tr>
<td>OS_XPORGREATER</td>
<td>18</td>
<td>Always returns <b>FALSE</b>.</td>
</tr>
<tr>
<td>OS_HOME</td>
<td>19</td>
<td>Always returns <b>FALSE</b>.</td>
</tr>
<tr>
<td>OS_PROFESSIONAL</td>
<td>20</td>
<td>The program is running on Windows NT Workstation or Windows 2000 (or one of its successors) Professional. Equivalent to <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_PLATFORM_WIN32_NT</a> &amp;&amp; <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_NT_WORKSTATION</a>.</td>
</tr>
<tr>
<td>OS_DATACENTER</td>
<td>21</td>
<td>The program is running on Windows Datacenter Server or Windows Server Datacenter Edition, any version. Equivalent to (<a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_NT_SERVER</a> || <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_NT_DOMAIN_CONTROLLER</a>) &amp;&amp; <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_SUITE_DATACENTER</a>.</td>
</tr>
<tr>
<td>OS_ADVSERVER</td>
<td>22</td>
<td>The program is running on Windows Advanced Server or Windows Server Enterprise Edition, any version. Equivalent to (<a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_NT_SERVER</a> || <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_NT_DOMAIN_CONTROLLER</a>) &amp;&amp; <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_SUITE_ENTERPRISE</a> &amp;&amp; !<a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_SUITE_DATACENTER</a>.</td>
</tr>
<tr>
<td>OS_SERVER</td>
<td>23</td>
<td>The program is running on Windows Server (Standard) or Windows Server Standard Edition, any version. This value will not return <b>true</b> for <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_SUITE_DATACENTER</a>, <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_SUITE_ENTERPRISE</a>, <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_SUITE_SMALLBUSINESS</a>, or <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_SUITE_SMALLBUSINESS_RESTRICTED</a>.</td>
</tr>
<tr>
<td>OS_TERMINALSERVER</td>
<td>24</td>
<td>The program is running on Windows 2000 Terminal Server in Application Server mode, or on Windows Server 2003  (or one of its successors) in Terminal Server mode. This is equivalent to <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_SUITE_TERMINAL</a> &amp;&amp; <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_SUITE_SINGLEUSERTS</a>.</td>
</tr>
<tr>
<td>OS_PERSONALTERMINALSERVER</td>
<td>25</td>
<td>The program is running on Windows XP (or one of its successors), Home Edition or Professional. This is equivalent to <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_SUITE_SINGLEUSERTS</a> &amp;&amp; !<a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_SUITE_TERMINAL</a>.</td>
</tr>
<tr>
<td>OS_FASTUSERSWITCHING</td>
<td>26</td>
<td>Fast user switching is enabled.</td>
</tr>
<tr>
<td>OS_WELCOMELOGONUI</td>
<td>27</td>
<td>Always returns <b>FALSE</b>.</td>
</tr>
<tr>
<td>OS_DOMAINMEMBER</td>
<td>28</td>
<td>The computer is joined to a domain.</td>
</tr>
<tr>
<td>OS_ANYSERVER</td>
<td>29</td>
<td>The program is running on any Windows Server product. Equivalent to <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_NT_SERVER</a> || <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_NT_DOMAIN_CONTROLLER</a>.</td>
</tr>
<tr>
<td>OS_WOW6432</td>
<td>30</td>
<td>The program is a 32-bit program running on 64-bit Windows.</td>
</tr>
<tr>
<td>OS_WEBSERVER</td>
<td>31</td>
<td>Always returns <b>FALSE</b>.</td>
</tr>
<tr>
<td>OS_SMALLBUSINESSSERVER</td>
<td>32</td>
<td>The program is running on Microsoft Small Business Server with restrictive client license in force. Equivalent to <a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">VER_SUITE_SMALLBUSINESS_RESTRICTED</a>.</td>
</tr>
<tr>
<td>OS_TABLETPC</td>
<td>33</td>
<td>The program is running on Windows XP Tablet PC Edition, or one of its successors.</td>
</tr>
<tr>
<td>OS_SERVERADMINUI</td>
<td>34</td>
<td>The user should be presented with administrator UI. It is possible to have server administrative UI on a non-server machine. This value informs the application that an administrator's profile has roamed to a non-server, and UI should be appropriate to an administrator. Otherwise, the user is shown a mix of administrator and nonadministrator settings.</td>
</tr>
<tr>
<td>OS_MEDIACENTER</td>
<td>35</td>
<td>The program is running on Windows XP Media Center Edition, or one of its successors. Equivalent to <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>(SM_MEDIACENTER).</td>
</tr>
<tr>
<td>OS_APPLIANCE</td>
<td>36</td>
<td>The program is running on Windows Appliance Server.</td>
</tr>
</table>

## -returns

Type: <b>BOOL</b>

Returns a nonzero value if the specified operating system or operating system feature is detected, otherwise <b>FALSE</b>.

## -remarks

Values are not provided for Windows Vista and Windows 7. To determine whether either of those operating systems are present, use <a href="/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa">VerifyVersionInfo</a>.

In Windows versions earlier than Windows Vista, <b>IsOS</b> was not exported by name or declared in a public header file. To use it in those cases, you must use <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> and request ordinal 437 from Shlwapi.dll to obtain a function pointer. Under Windows Vista, <b>IsOS</b> is included in Shlwapi.h and this is not necessary.

When referring to server products, "Windows Server" refers only to the Standard Edition server. If all server products are covered by a particular flag, it is called out explicitly in the table.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa">GetVersionEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa">VerifyVersionInfo</a>
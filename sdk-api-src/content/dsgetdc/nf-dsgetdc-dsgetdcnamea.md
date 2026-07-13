---
UID: NF:dsgetdc.DsGetDcNameA
title: DsGetDcNameA function (dsgetdc.h)
description: Returns the name of a domain controller in a specified domain. (ANSI)
helpviewer_keywords: ["DS_AVOID_SELF", "DS_BACKGROUND_ONLY", "DS_DIRECTORY_SERVICE_6_REQUIRED", "DS_DIRECTORY_SERVICE_8_REQUIRED", "DS_DIRECTORY_SERVICE_PREFERRED", "DS_DIRECTORY_SERVICE_REQUIRED", "DS_FORCE_REDISCOVERY", "DS_GC_SERVER_REQUIRED", "DS_GOOD_TIMESERV_PREFERRED", "DS_IP_REQUIRED", "DS_IS_DNS_NAME", "DS_IS_FLAT_NAME", "DS_KDC_REQUIRED", "DS_ONLY_LDAP_NEEDED", "DS_PDC_REQUIRED", "DS_RETURN_DNS_NAME", "DS_RETURN_FLAT_NAME", "DS_TIMESERV_REQUIRED", "DS_TRY_NEXTCLOSEST_SITE", "DS_WEB_SERVICE_REQUIRED", "DS_WRITABLE_REQUIRED", "DsGetDcNameA", "dsgetdc/DsGetDcNameA"]
old-location: ad\dsgetdcname.htm
tech.root: ad
ms.assetid: da8b2983-5e45-40b0-b552-c9b3a1d8ae94
ms.date: 12/05/2018
ms.keywords: DS_AVOID_SELF, DS_BACKGROUND_ONLY, DS_DIRECTORY_SERVICE_6_REQUIRED, DS_DIRECTORY_SERVICE_8_REQUIRED, DS_DIRECTORY_SERVICE_PREFERRED, DS_DIRECTORY_SERVICE_REQUIRED, DS_FORCE_REDISCOVERY, DS_GC_SERVER_REQUIRED, DS_GOOD_TIMESERV_PREFERRED, DS_IP_REQUIRED, DS_IS_DNS_NAME, DS_IS_FLAT_NAME, DS_KDC_REQUIRED, DS_ONLY_LDAP_NEEDED, DS_PDC_REQUIRED, DS_RETURN_DNS_NAME, DS_RETURN_FLAT_NAME, DS_TIMESERV_REQUIRED, DS_TRY_NEXTCLOSEST_SITE, DS_WEB_SERVICE_REQUIRED, DS_WRITABLE_REQUIRED, DsGetDcName, DsGetDcName function [Active Directory], DsGetDcNameA, DsGetDcNameW, _glines_dsgetdcname, ad.dsgetdcname, dsgetdc/DsGetDcName, dsgetdc/DsGetDcNameA, dsgetdc/DsGetDcNameW
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsGetDcNameW (Unicode) and DsGetDcNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NetApi32.lib
req.dll: NetApi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsGetDcNameA
 - dsgetdc/DsGetDcNameA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NetApi32.dll
 - logoncli.dll
api_name:
 - DsGetDcName
 - DsGetDcNameA
 - DsGetDcNameW
---

# DsGetDcNameA function


## -description

The <b>DsGetDcName</b> function returns the name of a 
   domain controller in a specified domain. This function accepts additional domain controller selection 
   criteria to indicate preference for a domain controller with particular characteristics.

## -parameters

### -param ComputerName [in]

Pointer to a null-terminated string that specifies the name of the server to process this function. 
      Typically, this parameter is <b>NULL</b>, which indicates that the local computer is 
      used.

### -param DomainName [in]

Pointer to a null-terminated string that specifies the name of the domain or application partition to 
       query. This name can either be a DNS style name, for example, fabrikam.com, or a flat-style name, for example, 
       Fabrikam. If a DNS style name is specified, the name may be specified with or without a trailing period.

If the <i>Flags</i> parameter contains the <b>DS_GC_SERVER_REQUIRED</b> 
       flag, <i>DomainName</i> must be the name of the forest. In this case, 
       <b>DsGetDcName</b> fails if <i>DomainName</i> 
       specifies a name that is not the forest root.

If the <i>Flags</i> parameter contains 
       the <b>DS_GC_SERVER_REQUIRED</b> flag and <i>DomainName</i> is 
       <b>NULL</b>, <b>DsGetDcName</b> attempts to 
       find a global catalog in the forest of the computer identified by <i>ComputerName</i>, which 
       is the local computer if <i>ComputerName</i> is <b>NULL</b>.

If <i>DomainName</i> is <b>NULL</b> and the 
       <i>Flags</i> parameter does not contain the <b>DS_GC_SERVER_REQUIRED</b> 
       flag, <i>ComputerName</i> is set to the default domain name of the primary domain of the 
       computer identified by <i>ComputerName</i>.

### -param DomainGuid [in]

Pointer to a <a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that specifies the 
    <b>GUID</b> of the domain queried. If <i>DomainGuid</i> is not 
  <b>NULL</b> and the domain specified by <i>DomainName</i> or 
  <i>ComputerName</i> cannot be found, 
  <b>DsGetDcName</b> attempts to locate a domain controller in the 
      domain having the GUID specified by <i>DomainGuid</i>.

### -param SiteName [in]

Pointer to a null-terminated string that specifies the name of the site where the returned domain 
      controller should physically exist. If this parameter is <b>NULL</b>, 
      <b>DsGetDcName</b> attempts to return a domain controller in the 
      site closest to the site of the computer specified by <i>ComputerName</i>. This parameter 
      should be <b>NULL</b>, by default.

### -param Flags [in]

Contains a set of flags that provide additional data used to process the request. This parameter can be a 
      combination of the following values.



#### DS_AVOID_SELF

When called from a domain controller, specifies that the returned domain controller name should not be 
        the current computer. If the current computer is not a domain controller, this flag is ignored. This flag can 
        be used to obtain the name of another domain controller in the domain.



#### DS_BACKGROUND_ONLY

If the <b>DS_FORCE_REDISCOVERY</b> flag is not specified,  this function uses cached 
        domain controller data.  If the cached data is more than 15 minutes old, the cache is refreshed by pinging the 
        domain controller.  If this flag is specified, this refresh is avoided even if the cached data is expired. 
        This flag should be used if the <b>DsGetDcName</b> function is 
        called periodically.



#### DS_DIRECTORY_SERVICE_PREFERRED

<b>DsGetDcName</b> attempts to find a  domain controller that 
        supports  directory service functions. If a domain controller that supports directory services is not 
        available, <b>DsGetDcName</b> returns the name of a 
        non-directory service domain controller. However, 
        <b>DsGetDcName</b>  only returns a non-directory service domain 
        controller after the attempt to find a directory service domain controller times out.



#### DS_DIRECTORY_SERVICE_REQUIRED

Requires that the returned domain controller support  directory services.



#### DS_DIRECTORY_SERVICE_6_REQUIRED

Requires that the returned domain controller be running Windows Server 2008 or later.



#### DS_DIRECTORY_SERVICE_8_REQUIRED

Requires that the returned domain controller be running Windows Server 2012 or later.



#### DS_FORCE_REDISCOVERY

Forces cached domain controller data to be ignored. When the <b>DS_FORCE_REDISCOVERY</b> 
         flag is not specified, <b>DsGetDcName</b> may return cached 
         domain controller data.  If this flag is specified, 
         <b>DsGetDcName</b> will not use cached information (if any 
         exists) but will instead perform a fresh domain controller discovery.

This flag should not be used under normal conditions, as using the cached domain controller information has 
         better performance characteristics and  helps to ensure that the same domain controller is used consistently 
         by all applications.  This flag should be used only after the application determines that the domain 
         controller returned by <b>DsGetDcName</b> (when called without 
         this flag) is not accessible.  In that case, the application should repeat the 
         <b>DsGetDcName</b> call with this flag to ensure that the 
         unuseful cached information (if any) is ignored and a reachable domain controller is discovered.



#### DS_GC_SERVER_REQUIRED

Requires that the returned domain controller be a global catalog server for the forest of domains with 
        this domain as the root. If this flag is set and the <i>DomainName</i> parameter is not 
        <b>NULL</b>, <i>DomainName</i> must specify a forest name. This flag 
        cannot be combined with the <b>DS_PDC_REQUIRED</b> or 
        <b>DS_KDC_REQUIRED</b> flags.



#### DS_GOOD_TIMESERV_PREFERRED

<b>DsGetDcName</b> attempts to find a domain controller that is 
        a reliable time server. The Windows Time Service can be configured to declare one or more domain controllers 
        as a reliable time server. For more information, see the 
        <a href="/previous-versions/windows/it-pro/windows-server-2003/cc773061(v=ws.10)">Windows Time Service</a> documentation. This 
        flag is intended to be used only by the Windows Time Service.



#### DS_IP_REQUIRED

This parameter indicates that the domain controller must have an IP address. In that case, 
        <b>DsGetDcName</b> will place the Internet protocol address of 
        the domain controller in the <b>DomainControllerAddress</b> member of 
        <i>DomainControllerInfo</i>.



#### DS_IS_DNS_NAME

Specifies that the <i>DomainName</i> parameter is a DNS name. This flag cannot be 
         combined with the <b>DS_IS_FLAT_NAME</b> flag.

Specify either <b>DS_IS_DNS_NAME</b> or <b>DS_IS_FLAT_NAME</b>. If 
          neither flag is specified, <b>DsGetDcName</b> may take longer 
          to find a domain controller because it may have to search for both the DNS-style and flat name.



#### DS_IS_FLAT_NAME

Specifies that the <i>DomainName</i> parameter is a flat name. This flag cannot be 
        combined with the <b>DS_IS_DNS_NAME</b> flag.



#### DS_KDC_REQUIRED

Requires that the returned domain controller be currently running the Kerberos Key Distribution Center 
        service. This flag cannot be combined with the <b>DS_PDC_REQUIRED</b> or 
        <b>DS_GC_SERVER_REQUIRED</b> flags.



#### DS_ONLY_LDAP_NEEDED

Specifies that the server returned is an LDAP server. The server returned is not necessarily a domain 
        controller. No other services are implied to be present at the server. The server returned does not 
        necessarily have a writable <b>config</b> container nor a writable 
        <b>schema</b> container. The server returned may not necessarily be used to create or 
        modify security principles. This flag may be used with the <b>DS_GC_SERVER_REQUIRED</b> 
        flag to return an LDAP server that also hosts a global catalog server. The returned global catalog server is 
        not necessarily a domain controller. No other services are implied to be present at the server. If this flag 
        is specified, the <b>DS_PDC_REQUIRED</b>, <b>DS_TIMESERV_REQUIRED</b>, 
        <b>DS_GOOD_TIMESERV_PREFERRED</b>, 
        <b>DS_DIRECTORY_SERVICES_PREFERED</b>, 
        <b>DS_DIRECTORY_SERVICES_REQUIRED</b>, and <b>DS_KDC_REQUIRED</b> flags 
        are ignored.



#### DS_PDC_REQUIRED

Requires that the returned domain controller be the primary domain controller for the domain. This flag 
        cannot be combined with the <b>DS_KDC_REQUIRED</b> or 
        <b>DS_GC_SERVER_REQUIRED</b> flags.



#### DS_RETURN_DNS_NAME

Specifies that the names returned in the <b>DomainControllerName</b> and 
        <b>DomainName</b> members of  <i>DomainControllerInfo</i> should be DNS 
        names. If a DNS name is not available, an error is returned. This flag cannot be specified with the 
        <b>DS_RETURN_FLAT_NAME</b> flag. This flag implies the 
        <b>DS_IP_REQUIRED</b> flag.



#### DS_RETURN_FLAT_NAME

Specifies that the names returned in the <b>DomainControllerName</b> and 
        <b>DomainName</b> members of  <i>DomainControllerInfo</i> should be 
        flat names. If a flat name is not available, an error is returned. This flag cannot be specified with the 
        <b>DS_RETURN_DNS_NAME</b> flag.



#### DS_TIMESERV_REQUIRED

Requires that the returned domain controller be currently running the Windows Time Service.



#### DS_TRY_NEXTCLOSEST_SITE

When this flag is specified, <b>DsGetDcName</b> attempts to 
         find a domain controller in the same site as the caller. If no such domain controller is found,  it will find 
         a domain controller that can provide topology information and call 
         <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindtoistga">DsBindToISTG</a> to obtain a bind handle, then call 
         <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsquerysitesbycosta">DsQuerySitesByCost</a> over  UDP to determine the 
         "next closest site," and finally cache the name of the site found. If no domain controller is found in that 
         site, then <b>DsGetDcName</b> falls back on the default method 
         of locating a domain controller.

If this flag is used in conjunction with   a non-NULL value in the input parameter 
         <i>SiteName</i>, then <b>ERROR_INVALID_FLAGS</b> is thrown.

Also, the kind of search employed with <b>DS_TRY_NEXT_CLOSEST_SITE</b> is site-specific, 
         so this flag is ignored if it is used in conjunction with <b>DS_PDC_REQUIRED</b>. Finally, 
         <b>DS_TRY_NEXTCLOSEST_SITE</b> is ignored when used in conjunction with 
         <b>DS_RETURN_FLAT_NAME</b> because  that uses NetBIOS to resolve the name, but the domain 
         of the domain controller found won't necessarily match the domain to which the client is joined.

<div class="alert"><b>Note</b>  This flag is Group Policy enabled.  If you enable the "Next Closest Site" policy setting, Next Closest 
         Site DC Location will be turned on for the machine across all available but un-configured network adapters. 
         If you disable the policy setting, Next Closest Site DC Location will not be used by default for the machine 
         across all available but un-configured network adapters. However, if a DC Locator call is made using the 
         <b>DS_TRY_NEXTCLOSEST_SITE</b> flag explicitly, 
         <b>DsGetDcName</b> honors the Next Closest Site behavior. If 
         you do not configure this policy setting, Next Closest Site DC Location will be not be used by default for 
         the machine across all available but un-configured network adapters. If the 
         <b>DS_TRY_NEXTCLOSEST_SITE</b> flag is used explicitly, the Next Closest Site behavior 
         will be used.</div>
<div> </div>


#### DS_WRITABLE_REQUIRED

Requires that the returned domain controller be writable; that is, host a writable copy of the directory 
        service.



#### DS_WEB_SERVICE_REQUIRED

Requires that the returned domain controller be currently running the Active Directory web service.

### -param DomainControllerInfo [out]

Pointer to a <b>PDOMAIN_CONTROLLER_INFO</b> value that receives a pointer to a 
      <a href="/windows/desktop/api/dsgetdc/ns-dsgetdc-domain_controller_infoa">DOMAIN_CONTROLLER_INFO</a> structure that contains 
      data  about the domain controller selected. This structure is allocated by 
      <b>DsGetDcName</b>. The caller must free the structure using the 
      <a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function when it is no longer 
      required.

## -returns

If the function returns domain controller data, the return value is 
       <b>ERROR_SUCCESS</b>.

If the function fails, the return value can be one of the following error codes.

## -remarks

The <b>DsGetDcName</b> function is sent to the Netlogon service 
    on the remote computer specified by <i>ComputerName</i>. If 
    <i>ComputerName</i> is <b>NULL</b>, the function is processed on the local 
    computer.

<b>DsGetDcName</b> does not verify that  the domain controller name 
     returned is the name of an actual domain controller or global catalog. If mutual authentication is required, the 
     caller must  perform the authentication.

<b>DsGetDcName</b> does not require any particular access to the 
     specified domain. By default, this function does not ensure that the returned domain controller is currently 
     available. Instead, the caller should attempt to use the returned domain controller. If the domain controller is 
     not available, the caller should call the <b>DsGetDcName</b> 
     function again, specifying the <b>DS_FORCE_REDISCOVERY</b> flag.

<h3><a id="Response_Time"></a><a id="response_time"></a><a id="RESPONSE_TIME"></a>Response Time</h3>
When using <b>DsGetDcName</b> be aware of the following timing 
      details:

<ul>
<li>
<b>DsGetDcName</b> makes network calls and can take from a few 
         seconds  up to one minute, depending on network traffic, topology, DC load, and so on.

</li>
<li>
It is NOT recommended to call <b>DsGetDcName</b> from a UI or 
        other timing critical thread.

</li>
<li>
The DC Locator does use optimized logic to provide the DC information as quickly as possible. It also uses 
        cached information at the site to contact the closest DC.

</li>
</ul>
<h3><a id="Notes_on_Domain_Controller_Stickiness"></a><a id="notes_on_domain_controller_stickiness"></a><a id="NOTES_ON_DOMAIN_CONTROLLER_STICKINESS"></a>Notes on Domain Controller Stickiness</h3>
In Active Directory Domain Services, the domain controller locator function is designed so that once a client 
      finds a preferred  domain controller, the client will not look for another unless that domain controller stops 
      responding or the client is restarted. This is referred to as "Domain Controller Stickiness." Because 
      workstations typically operate for months without a problem or restart,   one unintended consequence of this 
      behavior is that if a particular domain controller goes down for maintenance, all of the clients that were 
      connected to it shift their connections to another domain controller.  But when the domain controller comes back 
      up, no  clients ever reconnect to it because the clients do not restart very often.  This can cause 
      load-balancing problems.

Previously, the most common solution to this problem was to deploy a script on each client machine that 
      periodically called <b>DsGetDcName</b> using the 
      <code>DS_FORCE_REDISCOVERY</code> flag. This was a somewhat cumbersome solution, so 
      Windows Server 2008 and Windows Vista introduced a new mechanism that caused issues with  domain 
      controller stickiness.

Whenever <b>DsGetDcName</b> retrieves a domain controller name 
      from its cache, it checks to see if this cached entry is expired, and if so, discards that domain controller 
      name and tries to rediscover a domain controller name. The life span of a cached entry is controlled by the 
      value in the following registry keys


<b>HKEY_LOCAL_MACHINE</b>&#92;<b>SYSTEM</b>&#92;<b>CurrentControlSet</b>&#92;<b>Services</b>&#92;<b>Netlogon</b>&#92;<b>Parameters</b>&#92;<b>ForceRediscoveryInterval</b>



and


<b>HKEY_LOCAL_MACHINE</b>&#92;<b>Software</b>&#92;<b>Policies</b>&#92;<b>Microsoft</b>&#92;<b>Netlogon</b>&#92;<b>Parameters</b>&#92;<b>ForceRediscoveryInterval</b>



The values in these registry keys are of type <b>REG_DWORD</b>. They specify the length in 
      seconds before <b>DsGetDcName</b> should try to rediscover the 
      domain controller name. The default value is 43200 seconds (12 hours).  If the value of the 
      <b>ForceRediscoveryInterval</b> registry entry is set to 0, the client always 
  performs rediscovery. If the value is set to 4294967295, the cache never expires, and the cached domain controller 
  continues to be used. We recommend that you do not set the 
  <b>ForceRediscoveryInterval</b> registry entry to a value that is less than 3600 seconds 
  (60 minutes).

<div class="alert"><b>Note</b>  The registry settings of <b>ForceRediscoveryInterval</b> are group policy 
    enabled. If you disable the policy setting, Force Rediscovery will used by default for the machine at every 12 
  hour interval. If you do not configure this policy setting, Force Rediscovery will used by default for the machine 
  at every 12 hour interval, unless the local machine setting in the registry is a different value.</div>
<div> </div>
Note that if the <b>DS_BACKGROUND_ONLY</b> flag is specified, 
      <b>DsGetDcName</b> will never try to rediscover the domain 
      controller name, since the point of that flag is to force 
      <b>DsGetDcName</b> to use the cached domain controller name even 
      if it is expired.

<h3><a id="ETW_Tracing_in_DsGetDcName"></a><a id="etw_tracing_in_dsgetdcname"></a><a id="ETW_TRACING_IN_DSGETDCNAME"></a>ETW Tracing in DsGetDcName</h3>
To turn on <a href="/windows-hardware/drivers/hid/event-tracing">ETW Tracing</a> for 
      <b>DsGetDcName</b>, create the following registry key:


<b>HKEY_LOCAL_MACHINE</b>&#92;<b>System</b>&#92;<b>CurrentControlSet</b>&#92;<b>Services</b>&#92;<b>DCLocator</b>&#92;<b>Tracing</b>



The key will have a structure as follows:


```cpp
String ProcessName
  DWORD  PID <optional>
```


<i>ProcessName</i> must be the full name including extension of the process that you want 
      to get trace information for. <i>PID</i> is only required when multiple processes with the 
      same name exist.  If it is defined, then only the process with that PID will be enabled for tracing.  It is not 
      possible to trace only 2 out of 3 (or more) processes with the same name.  You can enable one instance or all 
      instances (when multiple instances with the same process name exist and PID is not specified, all instances will 
      be enabled for tracing).

For example, this would trace all instances of App1.exe and App2.exe, but only the instance of App3.exe that 
      has a PID of 999:


``` syntax
App1.exe 
App2.exe
App3.exe
     PID 999
```

Run the following command to start the tracing session:

<b>tracelog.exe -start &lt;sessionname&gt; -guid #cfaa5446-c6c4-4f5c-866f-31c9b55b962d -f &lt;filename&gt; -flag &lt;traceFlags&gt;</b>

<i>sessionname</i> is the name given for the trace session. The 
      <i>guid</i> for the DCLocator tracing provider is 
      "cfaa5446-c6c4-4f5c-866f-31c9b55b962d". <i>filename</i> is the name of the 
      log file to which the events are written. <i>traceFlags</i> is one or more of the following 
      flags which signify which areas to trace:

<table>
<tr>
<th>Flag</th>
<th>Hex Value</th>
<th>Description</th>
</tr>
<tr>
<td>
<b>DCLOCATOR_MISC</b>

</td>
<td>
0x00000002

</td>
<td>
Miscellaneous debugging

</td>
</tr>
<tr>
<td>
<b>DCLOCATOR_MAILSLOT</b>

</td>
<td>
0x00000010

</td>
<td>
Mailslot messages

</td>
</tr>
<tr>
<td>
<b>DCLOCATOR_SITE</b>

</td>
<td>
0x00000020

</td>
<td>
Sites

</td>
</tr>
<tr>
<td>
<b>DCLOCATOR_CRITICAL</b>

</td>
<td>
0x00000100

</td>
<td>
Important errors

</td>
</tr>
<tr>
<td>
<b>DCLOCATOR_SESSION_SETUP</b>

</td>
<td>
0x00000200

</td>
<td>
Trusted Domain Maintenance

</td>
</tr>
<tr>
<td>
<b>DCLOCATOR_DNS</b>

</td>
<td>
0x00004000

</td>
<td>
Name Registration

</td>
</tr>
<tr>
<td>
<b>DCLOCATOR_DNS_MORE</b>

</td>
<td>
0x00020000

</td>
<td>
Verbose Name Registration

</td>
</tr>
<tr>
<td>
<b>DCLOCATOR_MAILBOX_TEXT</b>

</td>
<td>
0x02000000

</td>
<td>
Verbose Mailbox Messages

</td>
</tr>
<tr>
<td>
<b>DCLOCATOR_SITE_MORE</b>

</td>
<td>
0x08000000

</td>
<td>
Verbose sites

</td>
</tr>
</table>
 

Run the following command to stop the trace session:

<b>tracelog.exe -stop &lt;sessionname&gt;</b>

<i>sessionname</i> is the same name as the name you used when starting the session.

<div class="alert"><b>Note</b>  The registry key for the process being traced must be present in the registry at the time the trace session 
      is started. When the session starts, the process will verify whether or not it should be generating trace 
      messages (based on the presence or absence of a registry key for that process name and optional PID). The 
      process checks the registry only at the start of the session. Any changes in the registry occurring after that 
      will not have any effect on tracing.</div>
<div> </div>




> [!NOTE]
> The dsgetdc.h header defines DsGetDcName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/dsgetdc/ns-dsgetdc-domain_controller_infoa">DOMAIN_CONTROLLER_INFO</a>



<a href="/windows/desktop/AD/directory-service-functions">Directory Service Functions</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetsitenamea">DsGetSiteName</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea">DsValidateSubnetName</a>



<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a>



<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>



<a href="/previous-versions/windows/it-pro/windows-server-2003/cc773061(v=ws.10)">Windows Time Service</a>

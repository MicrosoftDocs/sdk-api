---
UID: NF:dsparse.DsMakeSpnW
title: DsMakeSpnW function (dsparse.h)
description: Constructs a service principal name (SPN) that identifies a service instance. (Unicode)
helpviewer_keywords: ["DsMakeSpn", "DsMakeSpn function [Active Directory]", "DsMakeSpnW", "_glines_dsmakespn", "ad.dsmakespn", "dsparse/DsMakeSpn", "dsparse/DsMakeSpnW"]
old-location: ad\dsmakespn.htm
tech.root: ad
ms.assetid: fca3c59c-bb81-42a0-acd3-2e55c902febe
ms.date: 12/05/2018
ms.keywords: DsMakeSpn, DsMakeSpn function [Active Directory], DsMakeSpnA, DsMakeSpnW, _glines_dsmakespn, ad.dsmakespn, dsparse/DsMakeSpn, dsparse/DsMakeSpnA, dsparse/DsMakeSpnW
req.header: dsparse.h
req.include-header: Ntdsapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsMakeSpnW (Unicode) and DsMakeSpnA (ANSI)
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
 - DsMakeSpnW
 - dsparse/DsMakeSpnW
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
 - DsMakeSpn
 - DsMakeSpnA
 - DsMakeSpnW
---

# DsMakeSpnW function


## -description

The <b>DsMakeSpn</b> function constructs a service principal name (SPN) that identifies a service instance.

A client application uses this function to compose an SPN, which it uses to authenticate the service instance. For example, the client can pass an SPN in the <i>pszTargetName</i> parameter of the 
<a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext</a> function.

## -parameters

### -param ServiceClass [in]

Pointer to a constant null-terminated string that specifies the class of the service. This parameter can be any string unique to that service; either the protocol name, for example, ldap, or the string form of a GUID are acceptable.

### -param ServiceName [in]

Pointer to a constant null-terminated string that specifies the DNS name, NetBIOS name, or distinguished name (DN). This parameter must be non-<b>NULL</b>.

For more information about how the <i>ServiceName</i>, <i>InstanceName</i> and <i>InstancePort</i> parameters are used to compose an SPN, see the following Remarks section.

### -param InstanceName [in, optional]

Pointer to a constant null-terminated string that specifies the DNS name or IP address of the host for an instance of the service.

If <i>ServiceName</i> specifies the DNS or NetBIOS name of the service host computer, the <i>InstanceName</i> parameter must be <b>NULL</b>.

If <i>ServiceName</i> specifies a DNS domain name, the name of a DNS SRV record, or a distinguished name, such as the DN of a service connection point, the <i>InstanceName</i> parameter must specify the DNS or NetBIOS name of the service host computer.

### -param InstancePort [in]

Port number for an instance of the service. Use 0 for the default port. If this parameter is zero, the SPN does not include a port number.

### -param Referrer [in, optional]

Pointer to a constant null-terminated string that specifies the DNS name of the host that gave an IP address referral. This parameter is ignored unless the <i>ServiceName</i> parameter specifies an IP address.

### -param pcSpnLength [in, out]

Pointer to a variable that contains the length, in characters, of the buffer that will receive the new constructed SPN. This value may be 0 to request the final buffer size in advance.

The <i>pcSpnLength</i> parameter also receives the actual length of the SPN created, including the terminating null character.

### -param pszSpn [out]

Pointer to a null-terminated string that receives the constructed SPN. This buffer should be the length specified by <i>pcSpnLength</i>. The <i>pszSpn</i> parameter may be <b>NULL</b> to request the final buffer size in advance.

## -returns

If the function returns an SPN, the return value is <b>ERROR_SUCCESS</b>. If the function fails, the return value can be one of the following error codes.

## -remarks

The format of the SPN produced by the <b>DsMakeSpn</b> function depends on the input parameters. There are two basic formats. Both formats begin with the <i>ServiceClass</i> string followed by a host computer name and an optional <i>InstancePort</i> component.

<div class="alert"><b>Note</b>  This format is used by host-based services.</div>
<div> </div>
<p class="proch"><b>To produce an SPN with the "&lt;ServiceClass&gt;/&lt;host&gt;" format</b>

<ol>
<li>Set the <i>ServiceName</i> parameter to the DNS name of the host computer for the service instance. This is the host component of the SPN.</li>
<li>Set the <i>InstanceName</i> and <i>Referrer</i> parameters to <b>NULL</b>.</li>
<li>
Set the <i>InstancePort</i> parameter to zero. If <i>InstancePort</i> is nonzero, the SPN has the following format:


```cpp
<service class>/<host>:<instance port>/<referrer>
```


</li>
</ol>
<div class="alert"><b>Note</b>  This format is used by replicable services.</div>
<div> </div>
<p class="proch"><b>To produce an SPN with the "&lt;ServiceClass&gt;/&lt;host&gt;:&lt;InstancePort&gt;" format</b>

<ol>
<li>Set the <i>InstanceName</i> parameter to the DNS name of the host computer for the service instance. This is the host component.</li>
<li>Set the <i>ServiceName</i> parameter to a string that identifies an instance of the service. For example, it could be the distinguished name of the service connection point for this service instance.</li>
<li>Set the <i>Referrer</i> parameter to <b>NULL</b>.</li>
<li>
Set the <i>InstancePort</i> parameter to zero. If <i>InstancePort</i> is nonzero, the SPN has the following format:


```cpp
<service class>/<host>:<instance port>/<service name>
```


</li>
</ol>
The <i>Referrer</i> parameter is used only if the <i>ServiceName</i> parameter specifies the IP address of the service's host computer. In this case, <i>Referrer</i> specifies the DNS name of the computer that gave the IP address as a referral. The SPN has the following format:


```cpp
<service class>/<host>:<instance port>/<referrer>
```


where the host component is the <i>InstanceName</i> string or the <i>ServiceName</i> string if <i>InstanceName</i> is <b>NULL</b>, and the <i>InstancePort</i> component is optional.

String parameters cannot include the forward slash (/) character, as it is used to separate the components of the SPN.





> [!NOTE]
> The dsparse.h header defines DsMakeSpn as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext</a>

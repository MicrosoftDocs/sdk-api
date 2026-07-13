---
UID: NF:ntdsapi.DsGetSpnW
title: DsGetSpnW function (ntdsapi.h)
description: The DsGetSpn function constructs an array of one or more service principal names (SPNs). Each name in the array identifies an instance of a service. These SPNs may be registered with the directory service (DS) using the DsWriteAccountSpn function. (Unicode)
helpviewer_keywords: ["DS_SPN_DNS_HOST", "DS_SPN_DN_HOST", "DS_SPN_NB_HOST", "DS_SPN_DOMAIN", "DS_SPN_NB_DOMAIN", "DS_SPN_SERVICE", "DsGetSpn", "DsGetSpn function [Active Directory]", "DsGetSpnW", "_glines_dsgetspn", "ad.dsgetspn", "ntdsapi/DsGetSpn", "ntdsapi/DsGetSpnW"]
old-location: ad\dsgetspn.htm
tech.root: ad
ms.assetid: cbd53850-9b05-4f74-ab07-30dcad583fc5
ms.date: 12/05/2018
ms.keywords: DS_SPN_DNS_HOST,DS_SPN_DN_HOST,DS_SPN_NB_HOST, DS_SPN_DOMAIN,DS_SPN_NB_DOMAIN, DS_SPN_SERVICE, DsGetSpn, DsGetSpn function [Active Directory], DsGetSpnA, DsGetSpnW, _glines_dsgetspn, ad.dsgetspn, ntdsapi/DsGetSpn, ntdsapi/DsGetSpnA, ntdsapi/DsGetSpnW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsGetSpnW (Unicode) and DsGetSpnA (ANSI)
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
 - DsGetSpnW
 - ntdsapi/DsGetSpnW
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
 - DsGetSpn
 - DsGetSpnA
 - DsGetSpnW
---

# DsGetSpnW function


## -description

The <b>DsGetSpn</b> function constructs an array of one or more service principal names (SPNs). Each name in the array identifies an instance of a service. These SPNs may be registered with the directory service (DS) using the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dswriteaccountspna">DsWriteAccountSpn</a> function.

## -parameters

### -param ServiceType [in]

Identifies the format of the SPNs to compose. The <i>ServiceType</i> parameter can have one of the following values.



#### DS_SPN_DNS_HOST, DS_SPN_DN_HOST, DS_SPN_NB_HOST

The SPNs have the following format.


```cpp
ServiceClass/ InstanceName: InstancePort
```


The <i>ServiceName</i> parameter must be <b>NULL</b>. This is the SPN format for a host-based service, which provides services identified with its host computer. The <i>InstancePort</i> component is optional.



#### DS_SPN_DOMAIN, DS_SPN_NB_DOMAIN

The SPNs have the following format.


```cpp
ServiceClass/ InstanceName: InstancePort/ ServiceName
```


The <i>ServiceName</i> parameter must be the DNS name or DN of a domain. This format is used for a replicable service that provides services to the specified domain.



#### DS_SPN_SERVICE

The SPNs have the following format.


```cpp
ServiceClass/ InstanceName: InstancePort/ ServiceName
```


The <i>ServiceName</i> parameter must be a canonical DN or DNS name that identifies an instance of the service. For example, it could be a DNS name of a SRV record, or the distinguished name of the service connection point for this service instance.

### -param ServiceClass [in]

Pointer to a constant null-terminated string that specifies the class of the service; for example, http. Generally, this can be any string that is unique to the service.

### -param ServiceName [in, optional]

Pointer to a constant null-terminated string that specifies the DNS name or distinguished name (DN) of the service. <i>ServiceName</i> is not required for a host-based service. For more information, see the description of the <i>ServiceType</i> parameter for the possible values of <i>ServiceName</i>.

### -param InstancePort [in]

Specifies the port number of the service instance. If this value is zero, the SPN does not include a port number.

### -param cInstanceNames [in]

Specifies the number of elements in the <i>pInstanceNames</i> and <i>pInstancePorts</i> arrays. If this value is zero, <i>pInstanceNames</i> must point to an array of <i>cInstanceNames</i> strings, and <i>pInstancePorts</i> can be either <b>NULL</b> or a pointer to an array of <i>cInstanceNames</i> port numbers. If this value is zero, <b>DsGetSpn</b> returns only one SPN in the <i>prpszSpn</i> array and <i>pInstanceNames</i> and <i>pInstancePorts</i> are ignored.

### -param pInstanceNames [in, optional]

Pointer to an array of null-terminated strings that specify extra instance names (not used for host names). This parameter is ignored if <i>cInstanceNames</i> is zero. In that case, the <i>InstanceName</i> component of the SPN defaults to the fully qualified DNS name of the local computer or the NetBIOS name if <b>DS_SPN_NB_HOST</b> or <b>DS_SPN_NB_DOMAIN</b> is specified.

### -param pInstancePorts [in, optional]

Pointer to an array of extra instance ports. If this value is non-<b>NULL</b>, it must point to an array of <i>cInstanceNames</i> port numbers. If this value is <b>NULL</b>, the SPNs do not include a port number. This parameter is ignored if <i>cInstanceNames</i> is zero.

### -param pcSpn [out]

Pointer to a variable that receives the number of SPNs contained in <i>prpszSpn</i>.

### -param prpszSpn [out]

Pointer to a variable that receives a pointer to an array of SPNs. This array must be freed with 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreespnarraya">DsFreeSpnArray</a>.


##### - ServiceType.DS_SPN_DNS_HOST, DS_SPN_DN_HOST, DS_SPN_NB_HOST

The SPNs have the following format.


```cpp
ServiceClass/ InstanceName: InstancePort
```


The <i>ServiceName</i> parameter must be <b>NULL</b>. This is the SPN format for a host-based service, which provides services identified with its host computer. The <i>InstancePort</i> component is optional.


##### - ServiceType.DS_SPN_DOMAIN, DS_SPN_NB_DOMAIN

The SPNs have the following format.


```cpp
ServiceClass/ InstanceName: InstancePort/ ServiceName
```


The <i>ServiceName</i> parameter must be the DNS name or DN of a domain. This format is used for a replicable service that provides services to the specified domain.


##### - ServiceType.DS_SPN_SERVICE

The SPNs have the following format.


```cpp
ServiceClass/ InstanceName: InstancePort/ ServiceName
```


The <i>ServiceName</i> parameter must be a canonical DN or DNS name that identifies an instance of the service. For example, it could be a DNS name of a SRV record, or the distinguished name of the service connection point for this service instance.

## -returns

If the function returns an array of SPNs, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value can be one of the following error codes.

## -remarks

<p class="proch"><b>To create SPNs for multiple instances of a replicated service running on multiple host computers</b>

<ol>
<li>Set <i>cInstanceNames</i> to the number of instances.</li>
<li>Specify the names of the host computers in the <i>pInstanceNames</i> array.</li>
</ol>
<p class="proch"><b>To create SPNs for multiple instances of a service running on the same host computer</b>

<ol>
<li>Set the <i>cInstanceNames</i> to the number of instances.</li>
<li>Set each entry in the <i>pInstanceNames</i> array to the DNS name of the host computer.</li>
<li>Use the <i>pInstancePorts</i> parameter to specify an array of unique port numbers for each instance to disambiguate the SPNs.</li>
</ol>
String parameters cannot include the forward slash  (/), which is used to separate the components of the SPN.

An application with the appropriate privileges, which are usually those of a domain administrator, can call the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dswriteaccountspna">DsWriteAccountSpn</a> function to register one or more SPNs on the user or computer account where the service is running. Clients can then use the SPNs to authenticate the service.





> [!NOTE]
> The ntdsapi.h header defines DsGetSpn as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreespnarraya">DsFreeSpnArray</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dswriteaccountspna">DsWriteAccountSpn</a>

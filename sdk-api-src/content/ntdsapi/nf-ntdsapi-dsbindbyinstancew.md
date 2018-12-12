---
UID: NF:ntdsapi.DsBindByInstanceW
title: DsBindByInstanceW function
author: windows-sdk-content
description: Explicitly binds to any AD LDS or Active Directory instance.
old-location: adam\dsbindbyinstance.htm
tech.root: ADAM
ms.assetid: 65302ddc-2bc0-4d80-b028-e268859be227
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DsBindByInstance, DsBindByInstance function [ADAM], DsBindByInstanceA, DsBindByInstanceW, NTDSAPI_BIND_ALLOW_DELEGATION, NTDSAPI_BIND_FORCE_KERBEROS, adam.dsbindbyinstance, ntdsapi/DsBindByInstance, ntdsapi/DsBindByInstanceA, ntdsapi/DsBindByInstanceW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsBindByInstanceW (Unicode) and DsBindByInstanceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsBindByInstance
 - DsBindByInstanceA
 - DsBindByInstanceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: ADAM
---

# DsBindByInstanceW function


## -description


The <b>DsBindByInstance</b> function 
   explicitly binds to any AD LDS or Active Directory instance.


## -parameters




### -param ServerName [in]

Pointer to a null-terminated string that specifies the name of the instance. This parameter is required to 
      bind to an AD LDS instance. If this parameter is <b>NULL</b> when binding to an Active 
      Directory instance, then the <i>DnsDomainName</i> parameter must contain a value. If this 
      parameter and the <i>DnsDomainName</i> parameter are both <b>NULL</b>, the 
      function fails with the return value <b>ERROR_INVALID_PARAMETER</b> (87).


### -param Annotation [in]

Pointer to a null-terminated string that specifies the port number of the AD LDS instance or 
       <b>NULL</b> when binding to an Active Directory instance. For example, 
       "389".

If this parameter is <b>NULL</b> when binding by domain to an Active Directory instance, 
       then the <i>DnsDomainName</i> parameter must be specified. If this parameter is 
       <b>NULL</b> when binding to an AD LDS instance, then the 
       <i>InstanceGuid</i> parameter must be specified.


### -param InstanceGuid [in]

Pointer to a <b>GUID</b> value that contains the <b>GUID</b> of the AD LDS instance. The <b>GUID</b> value is the 
      <b>objectGUID</b> property of the <b>nTDSDSA</b> object of the 
      instance. If this parameter is <b>NULL</b> when binding to an AD LDS instance, the 
      <i>Annotation</i> parameter must be specified.


### -param DnsDomainName [in]

Pointer to a null-terminated string that specifies the DNS name of the domain when binding to an Active 
      Directory instance by domain. Set this parameter to <b>NULL</b> to bind to an Active 
      Directory instance by server or to an AD LDS instance.


### -param AuthIdentity [in, optional]

Handle to the credentials used to start the RPC session. Use the 
      <a href="https://msdn.microsoft.com/51aba58b-07c5-4e6d-8568-fa6f1a963d8e">DsMakePasswordCredentials</a> function to create 
      a structure suitable for <i>AuthIdentity</i>.


### -param ServicePrincipalName [in, optional]

Pointer to a null-terminated string that specifies the Service Principal Name to assign to the client. 
      Passing <b>NULL</b> in <i>ServicePrincipalName</i> is equivalent to a call 
      to the <a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a> function.


### -param BindFlags [in, optional]

Contains a set of flags that define the behavior of this function. This parameter can contain zero or a 
      combination of one or more of the following values.



#### NTDSAPI_BIND_ALLOW_DELEGATION (1)

Causes the bind to use the delegate impersonation level. This enables operations that require 
         delegation, such as <a href="https://msdn.microsoft.com/36ef8734-717a-4c3a-a839-6591d85c9734">DsAddSidHistory</a>, to succeed. 
         Specifying this flag also causes <a href="https://msdn.microsoft.com/52a5761d-5244-4bc9-8c09-fd08f10a9fff">DsBindWithSpnEx</a> to 
         operate similar to <a href="https://msdn.microsoft.com/9a149654-fd94-4b0c-b712-07fb827bef2f">DsBindWithSpn</a>.

If this flag is not specified, the bind will use the impersonate impersonation level. For more 
         information about impersonation levels, see 
         <a href="https://msdn.microsoft.com/en-us/library/ms686632(v=VS.85).aspx">Impersonation Levels</a>.

Most operations do not require the delegate impersonation level; this flag should only be 
         specified if it is required. Binding to a rogue server with the  delegate impersonation level enables the 
         rogue server to connect to a non-rogue server with your credentials and perform unintended operations.



#### NTDSAPI_BIND_FORCE_KERBEROS (4)

<b>Active Directory Lightweight Directory Services:  </b>If this flag is specified, <a href="https://msdn.microsoft.com/52a5761d-5244-4bc9-8c09-fd08f10a9fff">DsBindWithSpnEx</a> 
          requires Kerberos authentication to be used. If Kerberos authentication cannot be established, 
          <b>DsBindWithSpnEx</b> will not attempt to authenticate 
          with any other mechanism.


### -param phDS [out]

Address of a <b>HANDLE</b> value that receives the bind handle. To close this handle, 
      call <a href="https://msdn.microsoft.com/7106d67f-d421-4a7c-b775-440e5944f25e">DsUnBind</a>.


##### - BindFlags.NTDSAPI_BIND_ALLOW_DELEGATION (1)

Causes the bind to use the delegate impersonation level. This enables operations that require 
         delegation, such as <a href="https://msdn.microsoft.com/36ef8734-717a-4c3a-a839-6591d85c9734">DsAddSidHistory</a>, to succeed. 
         Specifying this flag also causes <a href="https://msdn.microsoft.com/52a5761d-5244-4bc9-8c09-fd08f10a9fff">DsBindWithSpnEx</a> to 
         operate similar to <a href="https://msdn.microsoft.com/9a149654-fd94-4b0c-b712-07fb827bef2f">DsBindWithSpn</a>.

If this flag is not specified, the bind will use the impersonate impersonation level. For more 
         information about impersonation levels, see 
         <a href="https://msdn.microsoft.com/en-us/library/ms686632(v=VS.85).aspx">Impersonation Levels</a>.

Most operations do not require the delegate impersonation level; this flag should only be 
         specified if it is required. Binding to a rogue server with the  delegate impersonation level enables the 
         rogue server to connect to a non-rogue server with your credentials and perform unintended operations.


##### - BindFlags.NTDSAPI_BIND_FORCE_KERBEROS (4)

<b>Active Directory Lightweight Directory Services:  </b>If this flag is specified, <a href="https://msdn.microsoft.com/52a5761d-5244-4bc9-8c09-fd08f10a9fff">DsBindWithSpnEx</a> 
          requires Kerberos authentication to be used. If Kerberos authentication cannot be established, 
          <b>DsBindWithSpnEx</b> will not attempt to authenticate 
          with any other mechanism.


## -returns



Returns <b>NO_ERROR</b> if successful or an RPC or Win32 error otherwise. Possible error codes include those 
      listed in the  following list.




## -remarks



The following list lists the required parameter values for binding to an instance.

<table>
<tr>
<th>Instance</th>
<th><i>ServerName</i></th>
<th><i>Annotation</i></th>
<th><i>InstanceGuid</i></th>
<th><i>DnsDomainName</i></th>
</tr>
<tr>
<td>
Active Directory by server

</td>
<td>
Server Name

</td>
<td>
<b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
</tr>
<tr>
<td>
Active Directory by domain

</td>
<td>
<b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
DNS domain name

</td>
</tr>
<tr>
<td>
AD LDS by port

</td>
<td>
DNS Name of the computer with the AD LDS installation.

</td>
<td>
Port Number

</td>
<td>
<b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
</tr>
<tr>
<td>
AD LDS by <b>GUID</b>

</td>
<td>
DNS Name of the computer with the AD LDS installation.

</td>
<td>
<b>NULL</b>

</td>
<td>
Instance <b>GUID</b>

</td>
<td>
<b>NULL</b>

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For improved performance when binding to an AD LDS instance on a computer with several instances 
     of AD LDS, bind by the Instance <b>GUID</b> instead of the port number.</div>
<div> </div>



---
UID: NS:wtypesbase._COAUTHINFO
title: "_COAUTHINFO"
author: windows-sdk-content
description: Contains the authentication settings used while making a remote activation request from the client computer to the server computer.
old-location: com\coauthinfo.htm
old-project: com
ms.assetid: 8cbe27b6-c676-49f2-8341-9e180c335636
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: COAUTHINFO, COAUTHINFO structure [COM], _COAUTHINFO, _com_COAUTHINFO, com.coauthinfo, wtypesbase/COAUTHINFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wtypesbase.h
req.include-header: WTypes.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: COAUTHINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wtypesbase.h
api_name:
-	COAUTHINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _COAUTHINFO structure


## -description


Contains the authentication settings used while making a remote activation request from the client computer to the server computer.


## -struct-fields




### -field dwAuthnSvc

The authentication service to be used. For a list of values, see <a href="https://msdn.microsoft.com/c16a8e52-a7f9-40d9-99ef-10b382b5cb3c">Authentication Service Constants</a>. Use RPC_C_AUTHN_NONE if no authentication is required. RPC_C_AUTHN_WINNT is the default and RPC_C_AUTHN_GSS_KERBEROS is also supported.


### -field dwAuthzSvc

The authorization service to be used. For a list of values, see <a href="https://msdn.microsoft.com/a0bc9337-b7e4-41c5-ae36-4843fa7d98ce">Authorization Constants</a>. To use the NT authentication service, specify RPC_C_AUTHZ_NONE.


### -field pwszServerPrincName

The server principal name to use with the authentication service. If you are using RPC_C_AUTHN_WINNT, the principal name must be <b>NULL</b>.


### -field dwAuthnLevel

The authentication level to be used. For a list of values, see <a href="https://msdn.microsoft.com/06c409e4-3772-45cf-8c31-c64f99aca244">Authentication Level Constants</a>.

As of Windows Server 2003, remote activations use the default authentication level specified in the <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> <i>dwAuthnLevel</i> parameter. In previous versions of Windows, RPC_C_AUTHN_LEVEL_CONNECT was always used for the security level unless another level was explicitly specified.


### -field dwImpersonationLevel

The impersonation level to be used. For a list of values, see <a href="https://msdn.microsoft.com/ea5a3b46-b607-4192-a3cc-b2ec55ca94a6">Impersonation Level Constants</a>. This value must be RPC_C_IMP_LEVEL_IMPERSONATE or above.


### -field pAuthIdentityData

A pointer to a <a href="https://msdn.microsoft.com/ce14f8a6-0495-491a-a5c7-de7c1d3efd95">COAUTHIDENTITY</a> structure that establishes a nondefault client identity. If this parameter is <b>NULL</b>, the actual identity of the client is used. Values of structure members are authentication-service specific. This value must be <b>NULL</b> if <b>dwAuthnSvc</b> does not specify either the NTLMSSP or Kerberos network authentication protocol is used as the authorization service.


### -field dwCapabilities

Indicates additional capabilities of this proxy. Currently, this member must be EOAC_NONE (0x0) or RPC_C_QOS_CAPABILITIES_MUTUAL_AUTH (0x1). Use RPC_C_QOS_CAPABILITIES_MUTUAL_AUTH if Kerberos is required.


## -remarks



If <b>pAuthInfo</b> in <a href="https://msdn.microsoft.com/88c94a7f-5cf0-4d61-833f-91cba45d8624">COSERVERINFO</a> is set to <b>NULL</b>, Snego will be used to negotiate an authentication service that will work between the client and server. However, a non-<b>NULL</b><b>COAUTHINFO</b> structure can be specified for <b>pAuthInfo</b> to meet any one of the following needs:

<ul>
<li>To specify a different client identity for computer remote activations. The specified identity will be used for the launch permission check on the server rather than the real client identity.
</li>
<li>To specify that Kerberos, rather than NTLMSSP, is used for machine remote activation. A nondefault client identity may or may not be specified. 
</li>
<li>To request unsecure activation.
</li>
<li>To specify a proprietary authentication service.</li>
</ul>
Specifying a <b>COAUTHINFO</b> structure allows DCOM activations to work correctly with security providers other than NTLMSSP. You can also specify additional security information used during remote activations for interoperability with alternate implementations of DCOM. 

If you set <b>dwAuthzSvc</b>, <b>pwszServerPrincName</b>, <b>dwImpersonationLevel</b>, or <b>dwCapabilities</b> to incorrect values and call either <a href="https://msdn.microsoft.com/65e758ce-50a4-49e8-b3b2-0cd148d2781a">CoGetClassObject</a> or <a href="https://msdn.microsoft.com/3b414b95-e8d2-42e8-b4f2-5cc5189a3d08">CoCreateInstanceEx</a>, these functions do not return E_INVALIDARG or a similar error. Default values are used instead of the incorrect values.




## -see-also




<a href="https://msdn.microsoft.com/88c94a7f-5cf0-4d61-833f-91cba45d8624">COSERVERINFO</a>
 

 


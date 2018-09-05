---
UID: NE:objidlbase.tagEOLE_AUTHENTICATION_CAPABILITIES
title: tagEOLE_AUTHENTICATION_CAPABILITIES
author: windows-sdk-content
description: Specifies various capabilities in CoInitializeSecurity and IClientSecurity::SetBlanket (or its helper function CoSetProxyBlanket).
old-location: com\eole_authentication_capabilities.htm
old-project: com
ms.assetid: cf3396d0-6674-4f12-bd4a-227a8d32bc92
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EOAC_ACCESS_CONTROL, EOAC_ANY_AUTHORITY, EOAC_APPID, EOAC_AUTO_IMPERSONATE, EOAC_DEFAULT, EOAC_DISABLE_AAA, EOAC_DYNAMIC, EOAC_DYNAMIC_CLOAKING, EOAC_MAKE_FULLSIC, EOAC_MUTUAL_AUTH, EOAC_NONE, EOAC_NO_CUSTOM_MARSHAL, EOAC_REQUIRE_FULLSIC, EOAC_SECURE_REFS, EOAC_STATIC_CLOAKING, EOLE_AUTHENTICATION_CAPABILITIES, EOLE_AUTHENTICATION_CAPABILITIES enumeration [COM], _com_EOLE_AUTHENTICATION_CAPABILITIES, com.eole_authentication_capabilities, objidlbase/EOAC_ACCESS_CONTROL, objidlbase/EOAC_ANY_AUTHORITY, objidlbase/EOAC_APPID, objidlbase/EOAC_AUTO_IMPERSONATE, objidlbase/EOAC_DEFAULT, objidlbase/EOAC_DISABLE_AAA, objidlbase/EOAC_DYNAMIC, objidlbase/EOAC_DYNAMIC_CLOAKING, objidlbase/EOAC_MAKE_FULLSIC, objidlbase/EOAC_MUTUAL_AUTH, objidlbase/EOAC_NONE, objidlbase/EOAC_NO_CUSTOM_MARSHAL, objidlbase/EOAC_REQUIRE_FULLSIC, objidlbase/EOAC_SECURE_REFS, objidlbase/EOAC_STATIC_CLOAKING, objidlbase/EOLE_AUTHENTICATION_CAPABILITIES, tagEOLE_AUTHENTICATION_CAPABILITIES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: objidlbase.h
req.include-header: Objidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: EOLE_AUTHENTICATION_CAPABILITIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - EOLE_AUTHENTICATION_CAPABILITIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# tagEOLE_AUTHENTICATION_CAPABILITIES enumeration


## -description


Specifies various capabilities in <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> and <a href="https://msdn.microsoft.com/adb35089-2846-4782-8c96-d3d1e14beed9">IClientSecurity::SetBlanket</a> (or its helper function <a href="https://msdn.microsoft.com/c2e5e681-8fa5-4b02-b59d-ba796eb0dccf">CoSetProxyBlanket</a>).


## -enum-fields




### -field EOAC_NONE

Indicates that no capability flags are set.


### -field EOAC_MUTUAL_AUTH

If this flag is specified, it will be ignored. Support for mutual authentication is automatically provided by some authentication services. See <a href="https://msdn.microsoft.com/a0c095a8-93b7-4350-aac6-a9a066cccffd">COM and Security Packages</a> for more information.


### -field EOAC_STATIC_CLOAKING

Sets static cloaking. When this flag is set, DCOM uses the thread token (if present) when determining the client's identity. However, the client's identity is determined on the first call on each proxy (if <a href="https://msdn.microsoft.com/adb35089-2846-4782-8c96-d3d1e14beed9">SetBlanket</a> is not called) and each time <a href="https://msdn.microsoft.com/c2e5e681-8fa5-4b02-b59d-ba796eb0dccf">CoSetProxyBlanket</a> is called on the proxy. For more information about static cloaking, see <a href="https://msdn.microsoft.com/5b97d9d6-8fa9-4da2-8351-64772227d9a2">Cloaking</a>.


<a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> and <a href="https://msdn.microsoft.com/adb35089-2846-4782-8c96-d3d1e14beed9">IClientSecurity::SetBlanket</a> return errors if both cloaking flags are set or if either flag is set when Schannel is the authentication service. 



### -field EOAC_DYNAMIC_CLOAKING

Sets dynamic cloaking. When this flag is set, DCOM uses the thread token (if present) when determining the client's identity. On each call to a proxy, the current thread token is examined to determine whether the client's identity has changed (incurring an additional performance cost) and the client is authenticated again only if necessary. Dynamic cloaking can be set by clients only. For more information about dynamic cloaking, see <a href="https://msdn.microsoft.com/5b97d9d6-8fa9-4da2-8351-64772227d9a2">Cloaking</a>.


<a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> and <a href="https://msdn.microsoft.com/adb35089-2846-4782-8c96-d3d1e14beed9">IClientSecurity::SetBlanket</a> return errors if both cloaking flags are set or if either flag is set when Schannel is the authentication service. 



### -field EOAC_ANY_AUTHORITY

This flag is obsolete.


### -field EOAC_MAKE_FULLSIC

Causes DCOM to send Schannel server principal names in fullsic format to clients as part of the default security negotiation. The name is extracted from the server certificate. For more information about the fullsic form, see <a href="https://msdn.microsoft.com/4d9977f8-0efb-4559-977e-3eba4e277bc0">Principal Names</a>.


### -field EOAC_DEFAULT

Tells DCOM to use the valid capabilities from the call to <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>. If <b>CoInitializeSecurity</b> was not called, EOAC_NONE will be used for the capabilities flag. This flag can be set only by clients in a call to <a href="https://msdn.microsoft.com/adb35089-2846-4782-8c96-d3d1e14beed9">IClientSecurity::SetBlanket</a> or <a href="https://msdn.microsoft.com/c2e5e681-8fa5-4b02-b59d-ba796eb0dccf">CoSetProxyBlanket</a>.


### -field EOAC_SECURE_REFS

Authenticates distributed reference count calls to prevent malicious users from releasing objects that are still being used. If this flag is set, which can be done only in a call to <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> by the client, the authentication level (in <i>dwAuthnLevel</i>) cannot be set to none.

The server always authenticates Release calls. Setting this flag prevents an authenticated client from releasing the objects of another authenticated client. It is recommended that clients always set this flag, although performance is affected because of the overhead associated with the extra security.


### -field EOAC_ACCESS_CONTROL

Indicates that the <i>pSecDesc</i> parameter to <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> is a pointer to an <a href="https://msdn.microsoft.com/f7f19a9d-27ed-479f-b5d4-562cab5be12a">IAccessControl</a> interface on an access control object. When DCOM makes security checks, it calls <a href="https://msdn.microsoft.com/ee9e7e2d-caec-443c-937d-b8fc64130ad4">IAccessControl::IsAccessAllowed</a>. This flag is set only by the server.


<a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> returns an error if both the EOAC_APPID and EOAC_ACCESS_CONTROL flags are set.


### -field EOAC_APPID

Indicates that the <i>pSecDesc</i> parameter to <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> is a pointer to a GUID that is an AppID. The <b>CoInitializeSecurity</b> function looks up the AppID in the registry and reads the security settings from there. If this flag is set, all other parameters to <b>CoInitializeSecurity</b> are ignored and must be zero. Only the server can set this flag.  For more information about this capability flag, see the Remarks section below.


<a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> returns an error if both the EOAC_APPID and EOAC_ACCESS_CONTROL flags are set.


### -field EOAC_DYNAMIC

Reserved.


### -field EOAC_REQUIRE_FULLSIC

Causes DCOM to fail <a href="https://msdn.microsoft.com/c2e5e681-8fa5-4b02-b59d-ba796eb0dccf">CoSetProxyBlanket</a> calls where an Schannel principal name is specified in any format other than fullsic. This flag is currently for clients only. For more information about the fullsic form, see <a href="https://msdn.microsoft.com/4d9977f8-0efb-4559-977e-3eba4e277bc0">Principal Names</a>.


### -field EOAC_AUTO_IMPERSONATE

Reserved.


### -field EOAC_DISABLE_AAA

Causes any activation where a server process would be launched under the caller's identity (activate-as-activator) to fail with E_ACCESSDENIED. This value, which can be specified only in a call to <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> by the client, allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.

An activation call that uses CLSCTX_ENABLE_AAA of the <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> enumeration will allow activate-as-activator activations for that call.


### -field EOAC_NO_CUSTOM_MARSHAL

Specifying this flag helps protect server security when using DCOM or COM+. It reduces the chances of executing arbitrary DLLs because it allows the marshaling of only CLSIDs that are implemented in Ole32.dll, ComAdmin.dll, ComSvcs.dll, or Es.dll, or that implement the CATID_MARSHALER category ID. Any service that is critical to system operation should set this flag.


### -field EOAC_RESERVED1




## -remarks



When the EOAC_APPID flag is set, <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> looks for the authentication level under the AppID. If the authentication level is not found, it looks for the default authentication level. If the default authentication level is not found, it generates a default authentication level of connect. If the authentication level is not RPC_C_AUTHN_LEVEL_NONE, <b>CoInitializeSecurity</b> looks for the access permission value under the AppID. If not found, it looks for the default access permission value. If not found, it generates a default access permission. All the other security settings are determined the same way as for a legacy application.

If the AppID is NULL, <b>CoInitializeSecurity</b> looks up the application .exe name in the registry and uses the AppID stored there. If the AppID does not exist, the machine defaults are used. 

The <a href="https://msdn.microsoft.com/adb35089-2846-4782-8c96-d3d1e14beed9">IClientSecurity::SetBlanket</a> method and <a href="https://msdn.microsoft.com/c2e5e681-8fa5-4b02-b59d-ba796eb0dccf">CoSetProxyBlanket</a> function return an error if any of the following flags are set in the capabilities parameter: EOAC_SECURE_REFS, EOAC_ACCESS_CONTROL, EOAC_APPID, EOAC_DYNAMIC, EOAC_REQUIRE_FULLSIC, EOAC_DISABLE_AAA, or EOAC_NO_CUSTOM_MARSHAL. 






## -see-also




<a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>



<a href="https://msdn.microsoft.com/c2e5e681-8fa5-4b02-b59d-ba796eb0dccf">CoSetProxyBlanket</a>



<a href="https://msdn.microsoft.com/f7f19a9d-27ed-479f-b5d4-562cab5be12a">IAccessControl</a>



<a href="https://msdn.microsoft.com/adb35089-2846-4782-8c96-d3d1e14beed9">IClientSecurity::SetBlanket</a>
 

 


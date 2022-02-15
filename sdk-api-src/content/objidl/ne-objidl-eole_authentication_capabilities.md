---
UID: NE:objidl.tagEOLE_AUTHENTICATION_CAPABILITIES
title: EOLE_AUTHENTICATION_CAPABILITIES (objidl.h)
description: Specifies various capabilities in CoInitializeSecurity and IClientSecurity::SetBlanket (or its helper function CoSetProxyBlanket).
helpviewer_keywords: ["EOAC_ACCESS_CONTROL","EOAC_ANY_AUTHORITY","EOAC_APPID","EOAC_AUTO_IMPERSONATE","EOAC_DEFAULT","EOAC_DISABLE_AAA","EOAC_DYNAMIC","EOAC_DYNAMIC_CLOAKING","EOAC_MAKE_FULLSIC","EOAC_MUTUAL_AUTH","EOAC_NONE","EOAC_NO_CUSTOM_MARSHAL","EOAC_REQUIRE_FULLSIC","EOAC_SECURE_REFS","EOAC_STATIC_CLOAKING","EOLE_AUTHENTICATION_CAPABILITIES","EOLE_AUTHENTICATION_CAPABILITIES enumeration [COM]","_com_EOLE_AUTHENTICATION_CAPABILITIES","com.eole_authentication_capabilities","objidlbase/EOAC_ACCESS_CONTROL","objidlbase/EOAC_ANY_AUTHORITY","objidlbase/EOAC_APPID","objidlbase/EOAC_AUTO_IMPERSONATE","objidlbase/EOAC_DEFAULT","objidlbase/EOAC_DISABLE_AAA","objidlbase/EOAC_DYNAMIC","objidlbase/EOAC_DYNAMIC_CLOAKING","objidlbase/EOAC_MAKE_FULLSIC","objidlbase/EOAC_MUTUAL_AUTH","objidlbase/EOAC_NONE","objidlbase/EOAC_NO_CUSTOM_MARSHAL","objidlbase/EOAC_REQUIRE_FULLSIC","objidlbase/EOAC_SECURE_REFS","objidlbase/EOAC_STATIC_CLOAKING","objidlbase/EOLE_AUTHENTICATION_CAPABILITIES"]
old-location: com\eole_authentication_capabilities.htm
tech.root: com
ms.assetid: cf3396d0-6674-4f12-bd4a-227a8d32bc92
ms.date: 12/05/2018
ms.keywords: EOAC_ACCESS_CONTROL, EOAC_ANY_AUTHORITY, EOAC_APPID, EOAC_AUTO_IMPERSONATE, EOAC_DEFAULT, EOAC_DISABLE_AAA, EOAC_DYNAMIC, EOAC_DYNAMIC_CLOAKING, EOAC_MAKE_FULLSIC, EOAC_MUTUAL_AUTH, EOAC_NONE, EOAC_NO_CUSTOM_MARSHAL, EOAC_REQUIRE_FULLSIC, EOAC_SECURE_REFS, EOAC_STATIC_CLOAKING, EOLE_AUTHENTICATION_CAPABILITIES, EOLE_AUTHENTICATION_CAPABILITIES enumeration [COM], _com_EOLE_AUTHENTICATION_CAPABILITIES, com.eole_authentication_capabilities, objidlbase/EOAC_ACCESS_CONTROL, objidlbase/EOAC_ANY_AUTHORITY, objidlbase/EOAC_APPID, objidlbase/EOAC_AUTO_IMPERSONATE, objidlbase/EOAC_DEFAULT, objidlbase/EOAC_DISABLE_AAA, objidlbase/EOAC_DYNAMIC, objidlbase/EOAC_DYNAMIC_CLOAKING, objidlbase/EOAC_MAKE_FULLSIC, objidlbase/EOAC_MUTUAL_AUTH, objidlbase/EOAC_NONE, objidlbase/EOAC_NO_CUSTOM_MARSHAL, objidlbase/EOAC_REQUIRE_FULLSIC, objidlbase/EOAC_SECURE_REFS, objidlbase/EOAC_STATIC_CLOAKING, objidlbase/EOLE_AUTHENTICATION_CAPABILITIES
req.header: objidl.h
req.include-header: Objidl.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: EOLE_AUTHENTICATION_CAPABILITIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEOLE_AUTHENTICATION_CAPABILITIES
 - objidl/tagEOLE_AUTHENTICATION_CAPABILITIES
 - EOLE_AUTHENTICATION_CAPABILITIES
 - objidl/EOLE_AUTHENTICATION_CAPABILITIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - EOLE_AUTHENTICATION_CAPABILITIES
---

# EOLE_AUTHENTICATION_CAPABILITIES enumeration


## -description

Specifies various capabilities in <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> and <a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket">IClientSecurity::SetBlanket</a> (or its helper function <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket">CoSetProxyBlanket</a>).

## -enum-fields

### -field EOAC_NONE:0

Indicates that no capability flags are set.

### -field EOAC_MUTUAL_AUTH:0x1

If this flag is specified, it will be ignored. Support for mutual authentication is automatically provided by some authentication services. See <a href="/windows/desktop/com/com-and-security-packages">COM and Security Packages</a> for more information.

### -field EOAC_STATIC_CLOAKING:0x20

Sets static cloaking. When this flag is set, DCOM uses the thread token (if present) when determining the client's identity. However, the client's identity is determined on the first call on each proxy (if <a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket">SetBlanket</a> is not called) and each time <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket">CoSetProxyBlanket</a> is called on the proxy. For more information about static cloaking, see <a href="/windows/desktop/com/cloaking">Cloaking</a>.


<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> and <a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket">IClientSecurity::SetBlanket</a> return errors if both cloaking flags are set or if either flag is set when Schannel is the authentication service.

### -field EOAC_DYNAMIC_CLOAKING:0x40

Sets dynamic cloaking. When this flag is set, DCOM uses the thread token (if present) when determining the client's identity. On each call to a proxy, the current thread token is examined to determine whether the client's identity has changed (incurring an additional performance cost) and the client is authenticated again only if necessary. Dynamic cloaking can be set by clients only. For more information about dynamic cloaking, see <a href="/windows/desktop/com/cloaking">Cloaking</a>.


<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> and <a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket">IClientSecurity::SetBlanket</a> return errors if both cloaking flags are set or if either flag is set when Schannel is the authentication service.

### -field EOAC_ANY_AUTHORITY:0x80

This flag is obsolete.

### -field EOAC_MAKE_FULLSIC:0x100

Causes DCOM to send Schannel server principal names in fullsic format to clients as part of the default security negotiation. The name is extracted from the server certificate. For more information about the fullsic form, see <a href="/windows/desktop/Rpc/principal-names">Principal Names</a>.

### -field EOAC_DEFAULT:0x800

Tells DCOM to use the valid capabilities from the call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>. If <b>CoInitializeSecurity</b> was not called, EOAC_NONE will be used for the capabilities flag. This flag can be set only by clients in a call to <a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket">IClientSecurity::SetBlanket</a> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket">CoSetProxyBlanket</a>.

### -field EOAC_SECURE_REFS:0x2

Authenticates distributed reference count calls to prevent malicious users from releasing objects that are still being used. If this flag is set, which can be done only in a call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> by the client, the authentication level (in <i>dwAuthnLevel</i>) cannot be set to none.

The server always authenticates Release calls. Setting this flag prevents an authenticated client from releasing the objects of another authenticated client. It is recommended that clients always set this flag, although performance is affected because of the overhead associated with the extra security.

### -field EOAC_ACCESS_CONTROL:0x4

Indicates that the <i>pSecDesc</i> parameter to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> is a pointer to an <a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a> interface on an access control object. When DCOM makes security checks, it calls <a href="/windows/desktop/api/iaccess/nf-iaccess-iaccesscontrol-isaccessallowed">IAccessControl::IsAccessAllowed</a>. This flag is set only by the server.


<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> returns an error if both the EOAC_APPID and EOAC_ACCESS_CONTROL flags are set.

### -field EOAC_APPID:0x8

Indicates that the <i>pSecDesc</i> parameter to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> is a pointer to a GUID that is an AppID. The <b>CoInitializeSecurity</b> function looks up the AppID in the registry and reads the security settings from there. If this flag is set, all other parameters to <b>CoInitializeSecurity</b> are ignored and must be zero. Only the server can set this flag.  For more information about this capability flag, see the Remarks section below.


<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> returns an error if both the EOAC_APPID and EOAC_ACCESS_CONTROL flags are set.

### -field EOAC_DYNAMIC:0x10

Reserved.

### -field EOAC_REQUIRE_FULLSIC:0x200

Causes DCOM to fail <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket">CoSetProxyBlanket</a> calls where an Schannel principal name is specified in any format other than fullsic. This flag is currently for clients only. For more information about the fullsic form, see <a href="/windows/desktop/Rpc/principal-names">Principal Names</a>.

### -field EOAC_AUTO_IMPERSONATE:0x400

Reserved.

### -field EOAC_DISABLE_AAA:0x1000

Causes any activation where a server process would be launched under the caller's identity (activate-as-activator) to fail with E_ACCESSDENIED. This value, which can be specified only in a call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> by the client, allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.

An activation call that uses CLSCTX_ENABLE_AAA of the <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-clsctx">CLSCTX</a> enumeration will allow activate-as-activator activations for that call.

### -field EOAC_NO_CUSTOM_MARSHAL:0x2000

Specifying this flag helps protect server security when using DCOM or COM+. It reduces the chances of executing arbitrary DLLs because it allows the marshaling of only CLSIDs that are implemented in Ole32.dll, ComAdmin.dll, ComSvcs.dll, or Es.dll, or that implement the CATID_MARSHALER category ID. Any service that is critical to system operation should set this flag.

### -field EOAC_RESERVED1:0x4000

## -remarks

When the EOAC_APPID flag is set, <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> looks for the authentication level under the AppID. If the authentication level is not found, it looks for the default authentication level. If the default authentication level is not found, it generates a default authentication level of connect. If the authentication level is not RPC_C_AUTHN_LEVEL_NONE, <b>CoInitializeSecurity</b> looks for the access permission value under the AppID. If not found, it looks for the default access permission value. If not found, it generates a default access permission. All the other security settings are determined the same way as for a legacy application.

If the AppID is NULL, <b>CoInitializeSecurity</b> looks up the application .exe name in the registry and uses the AppID stored there. If the AppID does not exist, the machine defaults are used. 

The <a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket">IClientSecurity::SetBlanket</a> method and <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket">CoSetProxyBlanket</a> function return an error if any of the following flags are set in the capabilities parameter: EOAC_SECURE_REFS, EOAC_ACCESS_CONTROL, EOAC_APPID, EOAC_DYNAMIC, EOAC_REQUIRE_FULLSIC, EOAC_DISABLE_AAA, or EOAC_NO_CUSTOM_MARSHAL.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket">CoSetProxyBlanket</a>



<a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a>



<a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket">IClientSecurity::SetBlanket</a>

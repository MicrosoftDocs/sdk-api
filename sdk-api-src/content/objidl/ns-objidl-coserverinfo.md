---
UID: NS:objidl._COSERVERINFO
title: COSERVERINFO (objidl.h)
description: The COSERVERINFO (objidl.h) structure identifies a remote computer resource to the activation functions.
helpviewer_keywords: ["COSERVERINFO","COSERVERINFO structure [COM]","_COSERVERINFO","_com_COSERVERINFO","com.coserverinfo","objidlbase/COSERVERINFO"]
old-location: com\coserverinfo.htm
tech.root: com
ms.assetid: 88c94a7f-5cf0-4d61-833f-91cba45d8624
ms.date: 08/13/2022
ms.keywords: COSERVERINFO, COSERVERINFO structure [COM], _COSERVERINFO, _com_COSERVERINFO, com.coserverinfo, objidlbase/COSERVERINFO
req.header: objidl.h
req.include-header: Objidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: COSERVERINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COSERVERINFO
 - objidl/_COSERVERINFO
 - COSERVERINFO
 - objidl/COSERVERINFO
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
 - COSERVERINFO
---

# COSERVERINFO structure


## -description

Identifies a remote computer resource to the activation functions.

## -struct-fields

### -field dwReserved1

This member is reserved and must be 0.

### -field pwszName

The name of the computer.

### -field pAuthInfo

A pointer to a <a href="/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo">COAUTHINFO</a> structure to override the default activation security for machine remote activations. Otherwise, set to <b>NULL</b> to indicate that default values should be used. For more information, see the Remarks section.

### -field dwReserved2

This member is reserved and must be 0.

## -remarks

The <b>COSERVERINFO</b> structure is used primarily to identify a remote system in object creation functions. Computer resources are named using the naming scheme of the network transport. By default, all UNC ("&#92;&#92;<i>server</i>" or "<i>server</i>") and DNS names ("<i>domain</i>.com", "<i>example</i>.microsoft.com", or "135.5.33.19") names are allowed. 



If <b>pAuthInfo</b> is set to <b>NULL</b>, <a href="/windows/desktop/com/snego">Snego</a> will be used to negotiate an authentication service that will work between the client and server. However, a non-<b>NULL</b><a href="/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo">COAUTHINFO</a> structure can be specified for <b>pAuthInfo</b> to meet any one of the following needs:

<ul>
<li>To specify a different client identity for computer remote activations. The specified identity will be used for the launch permission check on the server rather than the real client identity.
</li>
<li>To specify that Kerberos, rather than NTLMSSP, is used for machine remote activation. A nondefault client identity may or may not be specified. 
</li>
<li>To request unsecure activation.
</li>
<li>To specify a proprietary authentication service.</li>
</ul>
If <b>pAuthInfo</b> is not <b>NULL</b>, those values will be used to specify the authentication settings for the remote call. These settings will be passed to the <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa">RpcBindingSetAuthInfoEx</a> function.

If the <i>pAuthInfo</i> parameter is <b>NULL</b>, then <i>dwAuthnLevel</i> can be overridden by the authentication level set by the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> function. If the <b>CoInitializeSecurity</b> function isn't called, then the authentication level specified under the <a href="/windows/desktop/com/appid-key">AppID</a> registry key is used, if it exists.

Starting with Windows XP with Service Pack 2 (SP2), <i>dwAuthnLevel</i> is the maximum of RPC_C_AUTHN_LEVEL_CONNECT and the process-wide authentication level of the client process that is issuing the activation request. For earlier versions of the operating system, this is RPC_C_AUTHN_LEVEL_CONNECT.

## -see-also

<a href="/windows/desktop/com/activation-security">Activation Security</a>



<a href="/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo">COAUTHINFO</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject">CoGetClassObject</a>



<a href="/windows/desktop/api/objbase/nf-objbase-cogetinstancefromfile">CoGetInstanceFromFile</a>



<a href="/windows/desktop/api/objbase/nf-objbase-cogetinstancefromistorage">CoGetInstanceFromIStorage</a>



<a href="/windows/desktop/com/turning-off-activation-security">Turning Off Activation Security</a>

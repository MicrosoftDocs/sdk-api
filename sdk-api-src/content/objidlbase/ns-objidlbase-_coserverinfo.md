---
UID: NS:objidlbase._COSERVERINFO
title: "_COSERVERINFO"
author: windows-sdk-content
description: Identifies a remote computer resource to the activation functions.
old-location: com\coserverinfo.htm
old-project: com
ms.assetid: 88c94a7f-5cf0-4d61-833f-91cba45d8624
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: COSERVERINFO, COSERVERINFO structure [COM], _COSERVERINFO, _com_COSERVERINFO, com.coserverinfo, objidlbase/COSERVERINFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: objidlbase.h
req.include-header: Objidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: COSERVERINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	objidlbase.h
api_name:
-	COSERVERINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _COSERVERINFO structure


## -description


Identifies a remote computer resource to the activation functions. 


## -struct-fields




### -field dwReserved1

This member is reserved and must be 0.


### -field pwszName

The name of the computer.


### -field pAuthInfo

A pointer to a <a href="https://msdn.microsoft.com/8cbe27b6-c676-49f2-8341-9e180c335636">COAUTHINFO</a> structure to override the default activation security for machine remote activations. Otherwise, set to <b>NULL</b> to indicate that default values should be used. For more information, see the Remarks section.


### -field dwReserved2

This member is reserved and must be 0.


## -remarks



The <b>COSERVERINFO</b> structure is used primarily to identify a remote system in object creation functions. Computer resources are named using the naming scheme of the network transport. By default, all UNC ("\\<i>server</i>" or "<i>server</i>") and DNS names ("<i>domain</i>.com", "<i>example</i>.microsoft.com", or "135.5.33.19") names are allowed. 



If <b>pAuthInfo</b> is set to <b>NULL</b>, <a href="https://msdn.microsoft.com/2087a84c-d302-4511-9f02-2d20ee9e0d8e">Snego</a> will be used to negotiate an authentication service that will work between the client and server. However, a non-<b>NULL</b><a href="https://msdn.microsoft.com/8cbe27b6-c676-49f2-8341-9e180c335636">COAUTHINFO</a> structure can be specified for <b>pAuthInfo</b> to meet any one of the following needs:

<ul>
<li>To specify a different client identity for computer remote activations. The specified identity will be used for the launch permission check on the server rather than the real client identity.
</li>
<li>To specify that Kerberos, rather than NTLMSSP, is used for machine remote activation. A nondefault client identity may or may not be specified. 
</li>
<li>To request unsecure activation.
</li>
<li>To specify a proprietary authentication service.</li>
</ul>
If <b>pAuthInfo</b> is not <b>NULL</b>, those values will be used to specify the authentication settings for the remote call. These settings will be passed to the <a href="https://msdn.microsoft.com/2438816c-995e-4398-999d-48a3538eec18">RpcBindingSetAuthInfoEx</a> function.

If the <i>pAuthInfo</i> parameter is <b>NULL</b>, then <i>dwAuthnLevel</i> can be overridden by the authentication level set by the <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> function. If the <b>CoInitializeSecurity</b> function isn't called, then the authentication level specified under the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922446">AppID</a> registry key is used, if it exists.

Starting with Windows XP with Service Pack 2 (SP2), <i>dwAuthnLevel</i> is the maximum of RPC_C_AUTHN_LEVEL_CONNECT and the process-wide authentication level of the client process that is issuing the activation request. For earlier versions of the operating system, this is RPC_C_AUTHN_LEVEL_CONNECT.





## -see-also




<a href="https://msdn.microsoft.com/0c13d473-a9f9-40b5-951b-731eab736fe6">Activation Security</a>



<a href="https://msdn.microsoft.com/8cbe27b6-c676-49f2-8341-9e180c335636">COAUTHINFO</a>



<a href="https://msdn.microsoft.com/3b414b95-e8d2-42e8-b4f2-5cc5189a3d08">CoCreateInstanceEx</a>



<a href="https://msdn.microsoft.com/65e758ce-50a4-49e8-b3b2-0cd148d2781a">CoGetClassObject</a>



<a href="https://msdn.microsoft.com/f8a22f5f-a21f-49e7-bd6c-ca987206ee46">CoGetInstanceFromFile</a>



<a href="https://msdn.microsoft.com/6a77770c-b7e1-4d29-9c4b-331b5950a635">CoGetInstanceFromIStorage</a>



<a href="https://msdn.microsoft.com/3474f8ad-f041-4886-ad39-ff0603c5c69e">Turning Off Activation Security</a>
 

 


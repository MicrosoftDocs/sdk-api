---
UID: NF:winscard.SCardEstablishContext
title: SCardEstablishContext function
author: windows-sdk-content
description: Establishes the resource manager context (the scope) within which database operations are performed.
old-location: security\scardestablishcontext.htm
tech.root: secauthn
ms.assetid: 1cf9b005-b76c-4fc9-b4bd-a1ad8552535f
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: SCARD_SCOPE_SYSTEM, SCARD_SCOPE_USER, SCardEstablishContext, SCardEstablishContext function [Security], _smart_scardestablishcontext, security.scardestablishcontext, winscard/SCardEstablishContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
 - Ext-MS-Win-wlan-scard-l1-1-0.dll
 - Ext-MS-Win-Security-WinSCard-L1-1-0.dll
api_name:
 - SCardEstablishContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SCardEstablishContext function


## -description


The <b>SCardEstablishContext</b> function establishes the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a> (the scope) within which database operations are performed.


## -parameters




### -param dwScope [in]

Scope of the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_SCOPE_USER"></a><a id="scard_scope_user"></a><dl>
<dt><b>SCARD_SCOPE_USER</b></dt>
</dl>
</td>
<td width="60%">
Database operations are performed within the domain of the user.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_SCOPE_SYSTEM"></a><a id="scard_scope_system"></a><dl>
<dt><b>SCARD_SCOPE_SYSTEM</b></dt>
</dl>
</td>
<td width="60%">
Database operations are performed within the domain of the system. The calling application must have appropriate access permissions for any database actions.

</td>
</tr>
</table>
 


### -param pvReserved1 [in]

Reserved for future use and must be <b>NULL</b>. This parameter will allow a suitably privileged management application to act on behalf of another user.


### -param pvReserved2 [in]

Reserved for future use and must be <b>NULL</b>.


### -param phContext [out]

A handle to the established <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. This handle can now be supplied to other functions attempting to do work within this context.


## -returns



If the function succeeds, the function returns SCARD_S_SUCCESS. 

If the function fails, it returns an error code. For more information, see <a href="authentication_return_values.htm">Smart Card Return Values</a>. 




## -remarks



The context handle returned by <b>SCardEstablishContext</b> can be used by database query and management functions. For more information, see 
<a href="https://msdn.microsoft.com/a30cbb99-522c-4752-bfcd-75be608785f1">Smart Card Database Query Functions</a> and 
<a href="https://msdn.microsoft.com/a2f457e1-c042-42e7-9071-cf0edd68e27a">Smart Card Database Management Functions</a>.

To release an established resource manager context, use 
<a href="https://msdn.microsoft.com/aa17cf94-ca66-4b5e-b1cd-00319f496b09">SCardReleaseContext</a>.

If the client attempts a smart card operation in a remote session, such as a client session running on a terminal server, and the operating system in use does not support smart card redirection, this function returns ERROR_BROKEN_PIPE.


#### Examples

The following example establishes a resource manager context.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>SCARDCONTEXT    hSC;
LONG            lReturn;
// Establish the context.
lReturn = SCardEstablishContext(SCARD_SCOPE_USER,
                                NULL,
                                NULL,
                                &amp;hSC);
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardEstablishContext\n");
else
{
    // Use the context as needed. When done,
    // free the context by calling SCardReleaseContext.
    // ...
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/aa17cf94-ca66-4b5e-b1cd-00319f496b09">SCardReleaseContext</a>
 

 


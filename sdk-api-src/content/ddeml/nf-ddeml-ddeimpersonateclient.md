---
UID: NF:ddeml.DdeImpersonateClient
title: DdeImpersonateClient function (ddeml.h)
description: Impersonates a Dynamic Data Exchange (DDE) client application in a DDE client conversation.
helpviewer_keywords: ["DdeImpersonateClient","DdeImpersonateClient function [Data Exchange]","_win32_DdeImpersonateClient","_win32_ddeimpersonateclient_cpp","dataxchg.ddeimpersonateclient","ddeml/DdeImpersonateClient","winui._win32_ddeimpersonateclient"]
old-location: dataxchg\ddeimpersonateclient.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeimpersonateclient.htm
ms.date: 12/05/2018
ms.keywords: DdeImpersonateClient, DdeImpersonateClient function [Data Exchange], _win32_DdeImpersonateClient, _win32_ddeimpersonateclient_cpp, dataxchg.ddeimpersonateclient, ddeml/DdeImpersonateClient, winui._win32_ddeimpersonateclient
req.header: ddeml.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DdeImpersonateClient
 - ddeml/DdeImpersonateClient
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DdeImpersonateClient
---

# DdeImpersonateClient function


## -description

Impersonates a Dynamic Data Exchange (DDE) client application in a DDE client conversation.

## -parameters

### -param hConv [in]

Type: <b>HCONV</b>

A handle to the DDE client conversation to be impersonated.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Impersonation is the ability of a process to take on the security attributes of another process. When a client in a DDE conversation requests information from a DDE server, the server impersonates the client. When the server requests access to an object, the system verifies the access against the client's security attributes. 

When the impersonation is complete, the server normally calls the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself">RevertToSelf</a> function. 

<h3><a id="Security_Considerations"></a><a id="security_considerations"></a><a id="SECURITY_CONSIDERATIONS"></a>Security Considerations</h3>
If the call to <b>DdeImpersonateClient</b> fails for any reason, the client is not impersonated and the client request is made in the security context of the calling process. If the calling process is running as a highly privileged account, such as LocalSystem, or as a member of an administrative group, the user may be able to perform actions that would otherwise be disallowed. Therefore it is important that you always check the return value of the call, and if it fails to raise an error, do not continue execution of the client request.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient">ImpersonateNamedPipeClient</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself">RevertToSelf</a>
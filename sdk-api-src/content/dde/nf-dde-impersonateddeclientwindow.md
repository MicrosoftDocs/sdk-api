---
UID: NF:dde.ImpersonateDdeClientWindow
title: ImpersonateDdeClientWindow function (dde.h)
author: windows-sdk-content
description: Enables a Dynamic Data Exchange (DDE) server application to impersonate a DDE client application's security context. This protects secure server data from unauthorized DDE clients.
old-location: dataxchg\impersonateddeclientwindow.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange\dynamicdataexchangereference\dynamicdataexchangefunctions\impersonateddeclientwindow.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ImpersonateDdeClientWindow, ImpersonateDdeClientWindow function [Data Exchange], _win32_ImpersonateDdeClientWindow, _win32_impersonateddeclientwindow_cpp, dataxchg.impersonateddeclientwindow, dde/ImpersonateDdeClientWindow, winui._win32_impersonateddeclientwindow
ms.topic: function
req.header: dde.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - ImpersonateDdeClientWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImpersonateDdeClientWindow function


## -description


Enables a Dynamic Data Exchange (DDE) server application to impersonate a DDE client application's security context. This protects secure server data from unauthorized DDE clients. 


## -parameters




### -param hWndClient [in]

Type: <b>HWND</b>

A handle to the DDE client window to be impersonated. The client window must have established a DDE conversation with the server window identified by the 
					<i>hWndServer</i> parameter. 


### -param hWndServer [in]

Type: <b>HWND</b>

A handle to the DDE server window. An application must create the server window before calling this function. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



An application should call the <a href="https://msdn.microsoft.com/e3de77b9-dd27-4f20-b63d-ad2c57ac4283">RevertToSelf</a> function to undo the impersonation set by the <b>ImpersonateDdeClientWindow</b> function. 

A DDEML application should use the <a href="https://msdn.microsoft.com/en-us/library/ms648756(v=VS.85).aspx">DdeImpersonateClient</a> function. 

<h3><a id="Security_Considerations"></a><a id="security_considerations"></a><a id="SECURITY_CONSIDERATIONS"></a>Security Considerations</h3>
Using this function incorrectly might compromise the security of your program. It is very important to check the return value of the call. If the function fails for any reason, the client is not impersonated and any subsequent client request is made in the security context of the calling process. If the calling process is running as a highly privileged account, such as LocalSystem or as a member of an administrative group, the user may be able to perform actions that would otherwise be disallowed. Therefore, if the call fails or raises an error do not continue execution of the client request. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648774(v=VS.85).aspx">About Dynamic Data Exchange</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648756(v=VS.85).aspx">DdeImpersonateClient</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e3de77b9-dd27-4f20-b63d-ad2c57ac4283">RevertToSelf</a>
 

 


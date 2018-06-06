---
UID: NF:objbase.CoRevokeInitializeSpy
title: CoRevokeInitializeSpy function
author: windows-sdk-content
description: Revokes a registered implementation of the IInitializeSpy interface.
old-location: com\corevokeinitializespy.htm
old-project: com
ms.assetid: 24b0bedd-421a-4215-8edc-9fdce53e3b44
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: CoRevokeInitializeSpy, CoRevokeInitializeSpy function [COM], _com_CoRevokeInitializeSpy, com.corevokeinitializespy, objbase/CoRevokeInitializeSpy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: objbase.h
req.include-header: 
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
tech.root: 
req.typenames: COMSD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-private-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
 - API-MS-Win-Core-COM-Private-l1-1-1.dll
api_name:
 - CoRevokeInitializeSpy
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CoRevokeInitializeSpy function


## -description


Revokes a registered implementation of the <a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a> interface.


## -parameters




### -param uliCookie [in]

A <a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a> cookie identifying the registration.


## -returns



This function can return the standard return value E_INVALIDARG, as well as S_OK to indicate success.





## -remarks



<b>CoRevokeInitializeSpy</b> can only revoke cookies issued by previous calls to <a href="https://msdn.microsoft.com/1fd5606e-0a15-429a-b656-4620b873bec5">CoRegisterInitializeSpy</a> that were executed on the current thread. Using a cookie from another thread, or one that corresponds to an already revoked registration, will return E_INVALIDARG.



It is unpredictable whether a call to <b>CoRevokeInitializeSpy</b> from within an <a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a> method call will have an effect during the current top-level (non-nested) call to <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> or <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a>. The revocation will always have an effect after the current top-level call to <b>CoInitializeEx</b> or <b>CoUninitialize</b> returns.





## -see-also




<a href="https://msdn.microsoft.com/1fd5606e-0a15-429a-b656-4620b873bec5">CoRegisterInitializeSpy</a>



<a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a>
 

 


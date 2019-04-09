---
UID: NF:objbase.CoRegisterInitializeSpy
title: CoRegisterInitializeSpy function (objbase.h)
author: windows-sdk-content
description: Registers an implementation of the IInitializeSpy interface. The IInitializeSpy interface is defied to allow developers to perform initialization and cleanup on COM apartments.
old-location: com\coregisterinitializespy.htm
tech.root: com
ms.assetid: 1fd5606e-0a15-429a-b656-4620b873bec5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CoRegisterInitializeSpy, CoRegisterInitializeSpy function [COM], _com_CoRegisterInitializeSpy, com.coregisterinitializespy, objbase/CoRegisterInitializeSpy
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
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
 - CoRegisterInitializeSpy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoRegisterInitializeSpy function


## -description


Registers an implementation of the <a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a> interface. The <b>IInitializeSpy</b> interface is defied to allow developers to perform initialization and cleanup on COM apartments.


## -parameters




### -param pSpy [in]

A pointer to an instance of the <a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a> implementation.


### -param puliCookie [out]

The address at which to store a cookie that identifies this registration.


## -returns



This function can return the standard return value E_INVALIDARG, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The object was successfully registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support <a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a>.

</td>
</tr>
</table>
 




## -remarks



The <b>CoRegisterInitializeSpy</b> function registers an implementation of the <a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a> interface, which defines methods to be called when <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> (or <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a>) or <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a> is invoked.



<b>CoRegisterInitializeSpy</b> calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> for IID_InitializeSpy on <i>pSpy</i>. It stores the address of the returned interface pointer in thread-specific storage that is independent of the COM initialization state for this thread. On success, it stores in <i>puliCookie</i> a <a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a> cookie that represents this registration. Pass this cookie to <a href="https://msdn.microsoft.com/24b0bedd-421a-4215-8edc-9fdce53e3b44">CoRevokeInitializeSpy</a> to revoke the registration.




<a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a> implementations must deal with nesting issues caused by calling <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> or <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a> from within a notification method. Notifications occur only after the registration happens on this thread. For example, if <b>CoInitializeEx</b> is called before <b>CoRegisterInitializeSpy</b>, then the <a href="https://msdn.microsoft.com/f5b345d1-ab37-401a-9cb4-b01ef7254fc8">PreInitialize</a> and <a href="https://msdn.microsoft.com/bdef4089-93e6-4845-8dcc-1150d7a0d033">PostInitialize</a> notification methods will not be called.



Notification methods must not cause the failure of <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> or <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a> by throwing exceptions. Implementations of <a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a> must not propagate exceptions to code that calls <b>CoInitializeEx</b> or <b>CoUninitialize</b>. 



It is unpredictable whether a call to <b>CoRegisterInitializeSpy</b> from within an <a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a> method call will be effective during the current top-level (non-nested) call to <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> or <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a>. A registered implementation of <b>IInitializeSpy</b> will always be effective for future top-level calls to <b>CoInitializeEx</b> or <b>CoUninitialize</b>.




## -see-also




<a href="https://msdn.microsoft.com/24b0bedd-421a-4215-8edc-9fdce53e3b44">CoRevokeInitializeSpy</a>



<a href="https://msdn.microsoft.com/9cf1a3fa-dbc6-4760-a9e9-ef237737acfb">IInitializeSpy</a>
 

 


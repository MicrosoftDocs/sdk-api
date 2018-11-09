---
UID: NF:combaseapi.CoRevertToSelf
title: CoRevertToSelf function
author: windows-sdk-content
description: Restores the authentication information on a thread of execution.
old-location: com\coreverttoself.htm
tech.root: com
ms.assetid: 8061ddbe-ed21-47f7-9ac4-b3ec910ff89d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CoRevertToSelf, CoRevertToSelf function [COM], _com_CoRevertToSelf, com.coreverttoself, combaseapi/CoRevertToSelf
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
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
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoRevertToSelf
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoRevertToSelf function


## -description


Restores the authentication information on a thread of execution.


## -parameters






## -returns



This function supports the standard return values, including S_OK to indicate success.




## -remarks



<b>CoRevertToSelf</b>, which is a helper function that calls <a href="https://msdn.microsoft.com/en-us/library/ms680038(v=VS.85).aspx">IServerSecurity::RevertToSelf</a>, restores the authentication information on a thread to the authentication information on the thread before impersonation began.

<b>CoRevertToSelf</b> encapsulates the following common sequence of calls (error handling excluded):

<pre class="syntax" xml:space="preserve"><code>    CoGetCallContext(IID_IServerSecurity, (void**)&amp;pss);
    pss-&gt;RevertToSelf();
    pss-&gt;Release();
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691483(v=VS.85).aspx">CoGetCallContext</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680038(v=VS.85).aspx">IServerSecurity::RevertToSelf</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693319(v=VS.85).aspx">Security in COM</a>
 

 


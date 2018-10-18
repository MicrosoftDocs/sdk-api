---
UID: NN:shlobj.IDefViewFrame
title: IDefViewFrame
author: windows-sdk-content
description: Used only for its IUnknown functionality. It has no methods of its own.
old-location: shell\IDefViewFrame.htm
tech.root: shell
ms.assetid: 59dffa62-a26a-4dfa-95be-6b838a2d2903
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IDefViewFrame, IDefViewFrame interface [Windows Shell], IDefViewFrame interface [Windows Shell],described, _win32_IDefViewFrame, shell.IDefViewFrame, shlobj/IDefViewFrame
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDefViewFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDefViewFrame interface


## -description


Used only for its <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> functionality. It has no methods of its own.


## -remarks



<div class="alert"><b>Note</b>  This interface is supported through Windows XP Service Pack 3 (SP3) and Windows Server 2003. It is not supported in Windows Vista and later versions of Windows.</div>
<div> </div>
The IID for this interface is IID_IDefViewFrame. Use the service ID SID_DefView (defined in shlguid.h) in a call to <a href="_inet_IServiceProvider_QueryService_Method">QueryService</a> as shown in this example.

                

<pre class="syntax" xml:space="preserve"><code>HRESULT hr = isp-&gt;QueryService(punkSite, SID_DefView, IID_IDefViewFrame, (void**)&amp;pdvf);</code></pre>



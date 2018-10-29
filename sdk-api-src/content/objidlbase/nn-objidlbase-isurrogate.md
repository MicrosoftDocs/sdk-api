---
UID: NN:objidlbase.ISurrogate
title: ISurrogate
author: windows-sdk-content
description: Used to dynamically load new DLL servers into an existing surrogate and free the surrogate when it is no longer needed.
old-location: com\isurrogate.htm
tech.root: com
ms.assetid: fbed0514-3646-4744-aa7a-4a98f1a12cc0
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: ISurrogate, ISurrogate interface [COM], ISurrogate interface [COM],described, _com_isurrogate, com.isurrogate, objidlbase/ISurrogate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ISurrogate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISurrogate interface


## -description


Used to dynamically load new DLL servers into an existing surrogate and free the surrogate when it is no longer needed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISurrogate</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>ISurrogate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISurrogate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d897b02a-2540-4274-a0e3-e5c9299104a2">FreeSurrogate</a>
</td>
<td align="left" width="63%">
Unloads a DLL server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18727dee-392d-4f88-b1de-35da8a5887b6">LoadDllServer</a>
</td>
<td align="left" width="63%">
Loads a DLL server into the implementing surrogate.

</td>
</tr>
</table> 


## -remarks



A surrogate is an EXE process into which a DLL server can be loaded to give the DLL server the advantages of an EXE server without the coding overhead. It can also allow independent DLL servers to be located together within a single process, reducing the total number of processes needed. DLL servers are easy to write using standard development tools, like Microsoft Visual Studio, and running them in a surrogate process provides the benefits of an executable implementation, including fault isolation, the ability to serve multiple clients simultaneously, and allowing the server to provide services to remote clients in a distributed environment.




## -see-also




<a href="https://msdn.microsoft.com/fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44">DLL Surrogates</a>



<a href="https://msdn.microsoft.com/510e38e5-1965-46f4-b09c-6fa585cff993">Writing a Custom Surrogate</a>
 

 


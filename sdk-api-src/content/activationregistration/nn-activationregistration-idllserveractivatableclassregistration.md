---
UID: NN:activationregistration.IDllServerActivatableClassRegistration
title: IDllServerActivatableClassRegistration
author: windows-sdk-content
description: Enables getting the registration info for an in-process server.
old-location: winrt\idllserveractivatableclassregistration.htm
old-project: WinRT
ms.assetid: 00E9476E-45E0-4D97-9DA4-FD293674BED4
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IDllServerActivatableClassRegistration, IDllServerActivatableClassRegistration interface [Windows Runtime], IDllServerActivatableClassRegistration interface [Windows Runtime],described, activationregistration/IDllServerActivatableClassRegistration, winrt.idllserveractivatableclassregistration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: activationregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: ThreadingType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - activationregistration.h
api_name:
 - IDllServerActivatableClassRegistration
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDllServerActivatableClassRegistration interface


## -description


Enables getting  the registration info for an in-process server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDllServerActivatableClassRegistration</b> interface inherits from <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>. <b>IDllServerActivatableClassRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDllServerActivatableClassRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B46BB464-C993-49A7-86C8-4945E69AA9CC">DllPath</a>
</td>
<td align="left" width="63%">
Gets the fully qualified path to the in-process server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08F95AD6-B559-4652-A496-84777BF0189D">ThreadingType</a>
</td>
<td align="left" width="63%">
Gets the apartment threading model for activating the in-process server.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/99834A2D-547B-4B04-8703-46B11E0BB812">IActivatableClassRegistration</a>



<a href="https://msdn.microsoft.com/1D8F7B12-2883-478D-B83D-84AC47D512E4">IExeServerActivatableClassRegistration</a>



<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>
 

 


---
UID: NN:shobjidl_core.IApplicationActivationManager
title: IApplicationActivationManager
author: windows-sdk-content
description: Provides methods which activate Windows Store apps for the Launch, File, and Protocol extensions. You will normally use this interface in debuggers and design tools.
old-location: shell\IApplicationActivationManager.htm
old-project: shell
ms.assetid: 66C8EDC8-AF05-46d6-B29D-B6EE09DF6709
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IApplicationActivationManager, IApplicationActivationManager interface [Windows Shell], IApplicationActivationManager interface [Windows Shell],described, shell.IApplicationActivationManager, shobjidl_core/IApplicationActivationManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IApplicationActivationManager
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Browseui.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IApplicationActivationManager interface


## -description


Provides methods which activate Windows Store apps for the Launch, File, and Protocol <a href="https://msdn.microsoft.com/08800074-78ba-410a-962f-876da3463629">extensions</a>. You will normally use this interface in debuggers and design tools.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IApplicationActivationManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IApplicationActivationManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IApplicationActivationManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A39FA68E-F79F-454a-BB41-31D4D5EEC253">ActivateApplication</a>
</td>
<td align="left" width="63%">
Activates the specified Windows Store app for the generic launch contract (Windows.Launch) in the current session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E7EBB743-4847-4966-A2EA-486BBA6A4A6F">ActivateForFile</a>
</td>
<td align="left" width="63%">
Activates the specified Windows Store app for the file contract (Windows.File).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A37E140A-5369-4abe-A9E9-8BD2E4492082">ActivateForProtocol</a>
</td>
<td align="left" width="63%">
Activates the specified Windows Store app for the protocol contract (Windows.Protocol).

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Do not implement this interface yourself. Windows provides an implementation as part of the CApplicationActivationManager class. To get an instance of this class, call <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> with the CLSID_ApplicationActivationManager class ID.

<h3><a id="Usage_notes"></a><a id="usage_notes"></a><a id="USAGE_NOTES"></a>Usage notes</h3>
An <b>IApplicationActivationManager</b> object creates a thread in its host process to serve any activated event arguments objects (<a href="https://msdn.microsoft.com/609c711c-29e4-4ede-a035-5619611b40b2">LaunchActivatedEventArgs</a>, <a href="https://msdn.microsoft.com/511fcaf9-b3de-4f62-a26f-92a5b0575fd7">FileActivatedEventArgs</a>, and <a href="https://msdn.microsoft.com/03c9a412-01e3-49eb-b11c-a69156ed08a8">ProtocolActivatedEventArgs</a>) that are passed to the app. If the calling process is long-lived, you can create this object in-proc, based on the assumption that the event arguments will exist long enough for the target app to use them. However, if the calling process is spawned only to launch the target app, it should create the <b>IApplicationActivationManager</b> object out-of-process, by using CLSCTX_LOCAL_SERVER. This causes the object to be created in a Dllhost.exe instance that automatically manages the object's lifetime based on outstanding references to the activated event argument objects.




## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 


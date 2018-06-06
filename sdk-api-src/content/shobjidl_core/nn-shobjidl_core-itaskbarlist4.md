---
UID: NN:shobjidl_core.ITaskbarList4
title: ITaskbarList4
author: windows-sdk-content
description: Extends ITaskbarList3 by providing a method that allows the caller to control two property values for the tab thumbnail and peek feature.
old-location: shell\ITaskbarList4.htm
old-project: shell
ms.assetid: 7fc2c615-0bb0-4c03-9775-eee566c71088
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ITaskbarList4, ITaskbarList4 interface [Windows Shell], ITaskbarList4 interface [Windows Shell],described, _shell_ITaskbarList4, shell.ITaskbarList4, shobjidl_core/ITaskbarList4
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Explorerframe.dll
api_name:
 - ITaskbarList4
product: Windows
targetos: Windows
req.lib: Explorerframe.lib
req.dll: Explorerframe.dll
req.irql: 
req.product: Outlook Express 6.0
---

# ITaskbarList4 interface


## -description


Extends <a href="https://msdn.microsoft.com/a5eb4e5a-df17-4aca-96fb-d8475e266b92">ITaskbarList3</a> by providing a method that allows the caller to control two property values for the tab thumbnail and peek feature.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskbarList4</b> interface inherits from <a href="https://msdn.microsoft.com/a5eb4e5a-df17-4aca-96fb-d8475e266b92">ITaskbarList3</a>. <b>ITaskbarList4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITaskbarList4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc3fec4b-7770-44af-9892-239a17dd96b8">SetTabProperties</a>
</td>
<td align="left" width="63%">
Allows a tab to specify whether the main application frame window or the tab window should be used as a thumbnail or in the peek feature under certain circumstances.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38">ITaskbarList</a>, <a href="https://msdn.microsoft.com/8af23586-349f-4d21-98cb-0aaa27a586ff">ITaskbarList2</a>, and <a href="https://msdn.microsoft.com/a5eb4e5a-df17-4aca-96fb-d8475e266b92">ITaskbarList3</a> interfaces, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided in Windows as CLSID_TaskbarList. This interface is not implemented by third parties.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided in Windows as CLSID_TaskbarList. This interface is not implemented by third parties.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the methods of this interface for the following:
                

<ul>
<li>To use the thumbnail image of the application frame window in place of the tab thumbnail in some circumstances.</li>
<li>To use the application frame window in place of the tab as the source of the tab's peek image (a full-screen view of the window in response to a mouse-over event in the thumbnail).</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/a5eb4e5a-df17-4aca-96fb-d8475e266b92">ITaskbarList3</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 


---
UID: NN:shobjidl_core.IMenuBand
title: IMenuBand
author: windows-sdk-content
description: Exposes methods that allow a Component Object Model (COM) object to receive and translate appropriate messages.
old-location: shell\IMenuBand.htm
old-project: shell
ms.assetid: 67e12738-9951-4118-b968-7959cd175cf2
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMenuBand, IMenuBand interface [Windows Shell], IMenuBand interface [Windows Shell],described, _shell_IMenuBand, shell.IMenuBand, shobjidl_core/IMenuBand
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Shell32.dll
api_name:
 - IMenuBand
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IMenuBand interface


## -description


<p class="CCE_Message">[This interface is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be unsupported in subsequent versions of Windows.]

Exposes methods that allow a Component Object Model (COM) object to receive and translate appropriate messages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMenuBand</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMenuBand</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMenuBand</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d30a456c-7c09-4250-8509-353c54d017b9">IsMenuMessage</a>
</td>
<td align="left" width="63%">
A message pump calls this method to see if any messages should be redirected to the COM object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ee1f64f-ca8b-4f50-bbab-24ff1216708c">TranslateMenuMessage</a>
</td>
<td align="left" width="63%">
Translates a message for a COM object.

</td>
</tr>
</table> 


## -remarks



 An application can call <a href="https://www.bing.com/search?q=QueryService">QueryService</a> with one of the following service IDs. If the <i>riid</i> parameter of <b>QueryService</b> is IAccessible or IDispatch, the call to <b>QueryService</b> creates a new accessibility object. Otherwise, the call to <b>QueryService</b> is equivalent to a call to <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> with the service ID, as follows:



<table class="clsStd">
<tr>
<th>Service ID (SID)</th>
<th>Meaning</th>
</tr>
<tr>
<td>SID_SMenuBandChild</td>
<td>Retrieves the pointer to the <b>IMenuBand</b> interface for the submenu.</td>
</tr>
<tr>
<td>SID_SMenuBandParent</td>
<td>Retrieves the pointer to the <b>IMenuBand</b> interface for the parent menu.</td>
</tr>
<tr>
<td>SID_SMenuBandTop</td>
<td>Retrieves the pointer to the <b>IMenuBand</b> interface for the top menu.</td>
</tr>
</table>
 

In Windows 2000, this interface was implemented in browseui.dll. However, it is not recommended that this version be used.




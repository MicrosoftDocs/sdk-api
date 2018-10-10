---
UID: NN:wmiutils.IWbemPath
title: IWbemPath
author: windows-sdk-content
description: The IWbemPath interface is the primary interface for the object path parser and makes parsing a path available to programs in a standard way. This interface is the main interface for setting and retrieving path information.
old-location: wmi\iwbempath.htm
tech.root: WmiSdk
ms.assetid: 71b2597b-d82a-439d-b0b7-af76aefea6a2
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IWbemPath, IWbemPath interface [Windows Management Instrumentation], IWbemPath interface [Windows Management Instrumentation],described, WbemDefPath, _hmm_iwbempath, wmi.iwbempath, wmiutils/IWbemPath
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmiutils.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wmiutils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiutils.dll
api_name:
 - IWbemPath
 - IWbemPath.SetScopeFromText
 - WbemDefPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemPath interface


## -description


The 
<b>IWbemPath</b> interface is the primary interface for the object path parser and makes parsing a path available to programs in a standard way. This interface is the main interface for setting and retrieving path information.

The following table lists the methods for 
<b>IWbemPath</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemPath</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemPath</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemPath</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6826bd2a-6036-4017-a58e-621fc2361031">CreateClassPart</a>
</td>
<td align="left" width="63%">
Initializes the class/key portion of the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b79739b-b278-424f-ac3f-2bc769f3cf93">DeleteClassPart</a>
</td>
<td align="left" width="63%">
Deletes the class portion of the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7555d66-38d6-4d87-a241-6cce8674fa44">GetClassName</a>
</td>
<td align="left" width="63%">
Retrieves the class name from the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64f91184-668c-49ec-b8f9-aeeb7227ea6b">GetInfo</a>
</td>
<td align="left" width="63%">
Returns details about a path that has been placed into a parser object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf62727f-6ce7-4c7a-b757-c36d8cf64652">GetKeyList</a>
</td>
<td align="left" width="63%">
Retrieves an 
<a href="https://msdn.microsoft.com/5b188426-9d7f-4e87-9eed-ce80e5d93c30">IWbemPathKeyList</a> pointer so that the individual key may be accessed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5180c35-df90-447d-ad52-250ececfd525">GetNamespaceAt</a>
</td>
<td align="left" width="63%">
Retrieves a namespace based upon its index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce293b16-475c-48b7-a5c4-fa3575dd65a5">GetNamespaceCount</a>
</td>
<td align="left" width="63%">
Returns the number of namespaces in the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9601fb2b-583d-4481-8237-32db72432c63">GetScope</a>
</td>
<td align="left" width="63%">
Retrieves a scope based upon an index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f43d2215-7950-421b-b660-ebe89f24407e">GetScopeAsText</a>
</td>
<td align="left" width="63%">
Retrieves a scope in text format based upon an index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e818a4d-0a38-44ce-9027-2a94b7c86bef">GetScopeCount</a>
</td>
<td align="left" width="63%">
Returns the number of scopes in the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/831d34d8-d586-41cc-a878-7a2b837b84de">GetServer</a>
</td>
<td align="left" width="63%">
Returns the server portion of the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/427ff33a-3b46-481e-bf46-57b13d19332e">GetText</a>
</td>
<td align="left" width="63%">
Returns a textual representation of a path that has previously been placed into a parser object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28f33c70-095f-4bf0-98fa-29c5bb57f583">IsLocal</a>
</td>
<td align="left" width="63%">
Tests if the computer name passed in matches the computer name in the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7a2d585-98da-4f8f-b1df-bb961a1286f1">IsRelative</a>
</td>
<td align="left" width="63%">
Tests if the path is relative to a particular computer and namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95ba21af-3a43-4aa9-ab5b-90712e9cbed1">IsRelativeOrChild</a>
</td>
<td align="left" width="63%">
Tests if the path is relative to or a child of a particular computer and namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e0a907e-49d1-4775-885f-f059bb398804">IsSameClassName</a>
</td>
<td align="left" width="63%">
Tests whether the class name passed in matches the one in the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c42bdca5-fdc9-476a-9a32-1ac08e6dd6d0">RemoveAllNamespaces</a>
</td>
<td align="left" width="63%">
Removes the namespace portion of the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46c3215f-d038-4d0b-a9ce-b58e9381059e">RemoveAllScopes</a>
</td>
<td align="left" width="63%">
Removes all scopes from the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/425d26ee-c6f9-4562-9272-1c970fb6eb64">RemoveNamespaceAt</a>
</td>
<td align="left" width="63%">
Removes a namespace at a particular index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae7f4e88-32ca-45e1-8934-2801cfbe4cee">RemoveScope</a>
</td>
<td align="left" width="63%">
Removes a scope based on the index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77c51bb7-2868-4d9f-b48c-60b152e18cac">SetClassName</a>
</td>
<td align="left" width="63%">
Sets the class name portion of the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59e8d4bc-1bf6-4fe7-a269-22f0317b876c">SetNamespaceAt</a>
</td>
<td align="left" width="63%">
Sets a namespace's value in the path based upon an index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b4597ec-0d08-4929-9591-21588ded66bb">SetScope</a>
</td>
<td align="left" width="63%">
Sets a scope in the path based upon an index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>SetScopeFromText</b></td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4da66edf-bf38-4246-82fc-27fd14e7d183">SetServer</a>
</td>
<td align="left" width="63%">
Sets the server portion of the path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3ff2aa9-ffa8-4048-ac07-4b815b620d1f">SetText</a>
</td>
<td align="left" width="63%">
Parses a path so that information on the path can be returned by the path parser.

</td>
</tr>
</table> 


---
UID: NN:termmgr.ITPluggableTerminalSuperclassRegistration
title: ITPluggableTerminalSuperclassRegistration
author: windows-sdk-content
description: The ITPluggableTerminalSuperclassRegistration interface exposes methods that get and set information about a terminal superclass (name and CLSID).
old-location: tapi3\itpluggableterminalsuperclassregistration.htm
tech.root: tapi
ms.assetid: 76f5d213-d1fb-4437-af09-9d915db05dc6
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITPluggableTerminalSuperclassRegistration, ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2], ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2],described, _tapi3_itpluggableterminalsuperclassregistration, tapi3.itpluggableterminalsuperclassregistration, termmgr/ITPluggableTerminalSuperclassRegistration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: termmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPluggableTerminalSuperclassRegistration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPluggableTerminalSuperclassRegistration interface


## -description


The 
<b>ITPluggableTerminalSuperclassRegistration</b> interface exposes methods that get and set information about a terminal superclass (name and CLSID). The interface also includes methods that list all pluggable terminal public CLSIDs (terminal classes) registered below this terminal class.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPluggableTerminalSuperclassRegistration</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITPluggableTerminalSuperclassRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITPluggableTerminalSuperclassRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffef0255-c262-43d4-905f-5574c205c37e">Add</a>
</td>
<td align="left" width="63%">
Adds a pluggable terminal superclass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe87d55f-1e1c-4241-b8a3-b56d2000f3ca">Delete</a>
</td>
<td align="left" width="63%">
Deletes a terminal superclass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc75972d-7917-406d-8ed8-e05679ab86eb">EnumerateTerminalClasses</a>
</td>
<td align="left" width="63%">
Enumerates the terminal classes for the terminal superclass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d343284c-ffe1-4491-8476-37bcdd6e1a97">get_CLSID</a>
</td>
<td align="left" width="63%">
Gets the CLSID used to <b>CoCreateInstance</b> the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42f58ac2-4fda-436c-bbfd-d339296f736e">get_Name</a>
</td>
<td align="left" width="63%">
Gets the friendly name for the terminal superclass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/414ce7fe-e664-4915-84d6-0d4b6c750cf3">get_TerminalClasses</a>
</td>
<td align="left" width="63%">
Gets the terminal classes for the terminal superclass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e7ac968-c8b7-4af9-95b1-522e1b37c23a">GetTerminalSuperclassInfo</a>
</td>
<td align="left" width="63%">
Gets terminal superclass information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccb7159d-e838-408b-9565-a9854c4ba592">put_CLSID</a>
</td>
<td align="left" width="63%">
Sets the CLSID used to <b>CoCreateInstance</b> the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe9b569b-bfb7-401b-98a8-5db7f3739d41">put_Name</a>
</td>
<td align="left" width="63%">
Sets the friendly name for the terminal superclass.

</td>
</tr>
</table> 


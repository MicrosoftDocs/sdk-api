---
UID: NN:termmgr.ITPluggableTerminalSuperclassRegistration
title: ITPluggableTerminalSuperclassRegistration (termmgr.h)
author: windows-sdk-content
description: The ITPluggableTerminalSuperclassRegistration interface exposes methods that get and set information about a terminal superclass (name and CLSID).
old-location: tapi3\itpluggableterminalsuperclassregistration.htm
tech.root: Tapi
ms.assetid: 76f5d213-d1fb-4437-af09-9d915db05dc6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalSuperclassRegistration, ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2], ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2],described, _tapi3_itpluggableterminalsuperclassregistration, tapi3.itpluggableterminalsuperclassregistration, termmgr/ITPluggableTerminalSuperclassRegistration
ms.topic: interface
f1_keywords: 
 - "termmgr/ITPluggableTerminalSuperclassRegistration"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPluggableTerminalSuperclassRegistration interface


## -description


The 
<b>ITPluggableTerminalSuperclassRegistration</b> interface exposes methods that get and set information about a terminal superclass (name and CLSID). The interface also includes methods that list all pluggable terminal public CLSIDs (terminal classes) registered below this terminal class.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPluggableTerminalSuperclassRegistration</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITPluggableTerminalSuperclassRegistration</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalsuperclassregistration-add">Add</a>
</td>
<td align="left" width="63%">
Adds a pluggable terminal superclass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalsuperclassregistration-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes a terminal superclass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalsuperclassregistration-enumerateterminalclasses">EnumerateTerminalClasses</a>
</td>
<td align="left" width="63%">
Enumerates the terminal classes for the terminal superclass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalsuperclassregistration-get_clsid">get_CLSID</a>
</td>
<td align="left" width="63%">
Gets the CLSID used to <b>CoCreateInstance</b> the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalsuperclassregistration-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Gets the friendly name for the terminal superclass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalsuperclassregistration-get_terminalclasses">get_TerminalClasses</a>
</td>
<td align="left" width="63%">
Gets the terminal classes for the terminal superclass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalsuperclassregistration-getterminalsuperclassinfo">GetTerminalSuperclassInfo</a>
</td>
<td align="left" width="63%">
Gets terminal superclass information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalsuperclassregistration-put_clsid">put_CLSID</a>
</td>
<td align="left" width="63%">
Sets the CLSID used to <b>CoCreateInstance</b> the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalsuperclassregistration-put_name">put_Name</a>
</td>
<td align="left" width="63%">
Sets the friendly name for the terminal superclass.

</td>
</tr>
</table> 


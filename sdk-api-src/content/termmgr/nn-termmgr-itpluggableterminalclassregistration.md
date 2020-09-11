---
UID: NN:termmgr.ITPluggableTerminalClassRegistration
title: ITPluggableTerminalClassRegistration (termmgr.h)
description: The ITPluggableTerminalClassRegistration interface exposes methods that allow the creation, modification, and deletion of the registry entry for a pluggable terminal.
helpviewer_keywords: ["ITPluggableTerminalClassRegistration","ITPluggableTerminalClassRegistration interface [TAPI 2.2]","ITPluggableTerminalClassRegistration interface [TAPI 2.2]","described","_tapi3_itpluggableterminalclassregistration","tapi3.itpluggableterminalclassregistration","termmgr/ITPluggableTerminalClassRegistration"]
old-location: tapi3\itpluggableterminalclassregistration.htm
tech.root: tapi3
ms.assetid: 178824f5-9dda-4e8a-b921-f2c9d064a83c
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassRegistration, ITPluggableTerminalClassRegistration interface [TAPI 2.2], ITPluggableTerminalClassRegistration interface [TAPI 2.2],described, _tapi3_itpluggableterminalclassregistration, tapi3.itpluggableterminalclassregistration, termmgr/ITPluggableTerminalClassRegistration
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITPluggableTerminalClassRegistration
 - termmgr/ITPluggableTerminalClassRegistration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPluggableTerminalClassRegistration
---

# ITPluggableTerminalClassRegistration interface


## -description

The 
<b>ITPluggableTerminalClassRegistration</b> interface exposes methods that allow the creation, modification, and deletion of the registry entry for a pluggable terminal. (Each pluggable terminal must register itself in order to make the terminal available to applications.) The 
<b>ITPluggableTerminalClassRegistration</b> interface is created using COM <b>CoCreateInstance</b>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPluggableTerminalClassRegistration</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITPluggableTerminalClassRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITPluggableTerminalClassRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-add">Add</a>
</td>
<td align="left" width="63%">
Adds the terminal into the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes the terminal entry from the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-get_clsid">get_CLSID</a>
</td>
<td align="left" width="63%">
Gets the CLSID used to <b>CoCreateInstance</b> the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-get_company">get_Company</a>
</td>
<td align="left" width="63%">
Gets the name of the company that issued this pluggable terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-get_direction">get_Direction</a>
</td>
<td align="left" width="63%">
Gets the direction supported by the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-get_mediatypes">get_MediaTypes</a>
</td>
<td align="left" width="63%">
Gets the media types supported by the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Gets the terminal's friendly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-get_terminalclass">get_TerminalClass</a>
</td>
<td align="left" width="63%">
Gets the terminal's terminal class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-get_version">get_Version</a>
</td>
<td align="left" width="63%">
Gets the terminal version.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-getterminalclassinfo">GetTerminalClassInfo</a>
</td>
<td align="left" width="63%">
Gets all information from the registry for a specific terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-put_clsid">put_CLSID</a>
</td>
<td align="left" width="63%">
Sets the CLSID used to <b>CoCreateInstance</b> the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-put_company">put_Company</a>
</td>
<td align="left" width="63%">
Sets the name of the company that issued this pluggable terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-put_direction">put_Direction</a>
</td>
<td align="left" width="63%">
Sets the direction supported by the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-put_mediatypes">put_MediaTypes</a>
</td>
<td align="left" width="63%">
Sets the media types supported by the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-put_name">put_Name</a>
</td>
<td align="left" width="63%">
Sets the terminal's friendly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-put_terminalclass">put_TerminalClass</a>
</td>
<td align="left" width="63%">
Sets the terminal's terminal class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-put_version">put_Version</a>
</td>
<td align="left" width="63%">
Sets the terminal version.

</td>
</tr>
</table>


---
UID: NN:tapi3if.ITPluggableTerminalClassInfo
title: ITPluggableTerminalClassInfo (tapi3if.h)
description: The ITPluggableTerminalClassInfo interface exposes methods that allow the application to retrieve information concerning a pluggable terminal.
helpviewer_keywords: ["ITPluggableTerminalClassInfo","ITPluggableTerminalClassInfo interface [TAPI 2.2]","ITPluggableTerminalClassInfo interface [TAPI 2.2]","described","_tapi3_itpluggableterminalclassinfo","tapi3.itpluggableterminalclassinfo","tapi3if/ITPluggableTerminalClassInfo"]
old-location: tapi3\itpluggableterminalclassinfo.htm
tech.root: tapi3
ms.assetid: 0f7190c4-c696-4749-82f2-20fdbc8651f4
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassInfo, ITPluggableTerminalClassInfo interface [TAPI 2.2], ITPluggableTerminalClassInfo interface [TAPI 2.2],described, _tapi3_itpluggableterminalclassinfo, tapi3.itpluggableterminalclassinfo, tapi3if/ITPluggableTerminalClassInfo
req.header: tapi3if.h
req.include-header: Tapi3.h
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
 - ITPluggableTerminalClassInfo
 - tapi3if/ITPluggableTerminalClassInfo
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
 - ITPluggableTerminalClassInfo
---

# ITPluggableTerminalClassInfo interface


## -description

The 
<b>ITPluggableTerminalClassInfo</b> interface exposes methods that allow the application to retrieve information concerning a pluggable terminal.

The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ienumpluggableterminalclassinfo-next">IEnumPluggableTerminalClassInfo::Next</a> and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport2-get_pluggableterminalclasses">ITTerminalSupport2::get_PluggableTerminalClasses</a> methods create the 
<b>ITPluggableTerminalClassInfo</b> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPluggableTerminalClassInfo</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITPluggableTerminalClassInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITPluggableTerminalClassInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itpluggableterminalclassinfo-get_clsid">get_CLSID</a>
</td>
<td align="left" width="63%">
Gets the CLSID used to CoCreateInstance the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itpluggableterminalclassinfo-get_company">get_Company</a>
</td>
<td align="left" width="63%">
Gets the name of the company that issued this pluggable terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itpluggableterminalclassinfo-get_direction">get_Direction</a>
</td>
<td align="left" width="63%">
Gets the direction supported by the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itpluggableterminalclassinfo-get_mediatypes">get_MediaTypes</a>
</td>
<td align="left" width="63%">
Gets the media types supported by the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itpluggableterminalclassinfo-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Gets the terminal's friendly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itpluggableterminalclassinfo-get_terminalclass">get_TerminalClass</a>
</td>
<td align="left" width="63%">
Gets the terminal's terminal class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itpluggableterminalclassinfo-get_version">get_Version</a>
</td>
<td align="left" width="63%">
Gets the terminal version.

</td>
</tr>
</table>
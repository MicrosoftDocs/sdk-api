---
UID: NN:tapi3if.ITPluggableTerminalSuperclassInfo
title: ITPluggableTerminalSuperclassInfo (tapi3if.h)

description: The ITPluggableTerminalSuperclassInfo interface exposes methods that get the name and CLSID of a pluggable terminal class.
old-location: tapi3\itpluggableterminalsuperclassinfo.htm
tech.root: Tapi
ms.assetid: f9226af1-90e7-4317-af73-e1563883e2b6

ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalSuperclassInfo, ITPluggableTerminalSuperclassInfo interface [TAPI 2.2], ITPluggableTerminalSuperclassInfo interface [TAPI 2.2],described, _tapi3_itpluggableterminalsuperclassinfo, tapi3.itpluggableterminalsuperclassinfo, tapi3if/ITPluggableTerminalSuperclassInfo
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITPluggableTerminalSuperclassInfo"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPluggableTerminalSuperclassInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPluggableTerminalSuperclassInfo interface


## -description


The 
<b>ITPluggableTerminalSuperclassInfo</b> interface exposes methods that get the name and CLSID of a pluggable terminal class. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumpluggablesuperclassinfo-next">IEnumPluggableSuperclassInfo::Next</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport2-get_pluggablesuperclasses">ITTerminalSupport2::get_PluggableSuperclasses</a> methods create the 
<b>ITPluggableTerminalSuperclassInfo</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPluggableTerminalSuperclassInfo</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITPluggableTerminalSuperclassInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITPluggableTerminalSuperclassInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itpluggableterminalsuperclassinfo-get_clsid">get_CLSID</a>
</td>
<td align="left" width="63%">
Gets the CLSID used to <b>CoCreateInstance</b> the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itpluggableterminalsuperclassinfo-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Gets the terminal's friendly name.

</td>
</tr>
</table> 


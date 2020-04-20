---
UID: NN:tapi3if.IEnumPluggableTerminalClassInfo
title: IEnumPluggableTerminalClassInfo (tapi3if.h)
description: The IEnumPluggableTerminalClassInfo interface provides COM-standard enumeration methods for the ITPluggableTerminalClassInfo interface. The ITTerminalSupport2::EnumeratePluggableTerminalClasses method returns a pointer to IEnumPluggableTerminalClassInfo.helpviewer_keywords: ["IEnumPluggableTerminalClassInfo","IEnumPluggableTerminalClassInfo interface [TAPI 2.2]","IEnumPluggableTerminalClassInfo interface [TAPI 2.2]","described","_tapi3_ienumpluggableterminalclassinfo","tapi3.ienumpluggableterminalclassinfo","tapi3if/IEnumPluggableTerminalClassInfo"]
old-location: tapi3\ienumpluggableterminalclassinfo.htm
tech.root: Tapi
ms.assetid: 72c0db41-8391-4923-8961-6aefce9886c4
ms.date: 12/05/2018
ms.keywords: IEnumPluggableTerminalClassInfo, IEnumPluggableTerminalClassInfo interface [TAPI 2.2], IEnumPluggableTerminalClassInfo interface [TAPI 2.2],described, _tapi3_ienumpluggableterminalclassinfo, tapi3.ienumpluggableterminalclassinfo, tapi3if/IEnumPluggableTerminalClassInfo
f1_keywords:
- tapi3if/IEnumPluggableTerminalClassInfo
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
- IEnumPluggableTerminalClassInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumPluggableTerminalClassInfo interface


## -description


The 
<b>IEnumPluggableTerminalClassInfo</b> interface provides COM-standard enumeration methods for the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo">ITPluggableTerminalClassInfo</a> interface. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport2-enumeratepluggableterminalclasses">ITTerminalSupport2::EnumeratePluggableTerminalClasses</a> method returns a pointer to 
<b>IEnumPluggableTerminalClassInfo</b>.

The 
<b>IEnumPluggableTerminalClassInfo</b> interface is hidden from Visual Basic and scripting languages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumPluggableTerminalClassInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumPluggableTerminalClassInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumPluggableTerminalClassInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumpluggableterminalclassinfo-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumpluggableterminalclassinfo-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumpluggableterminalclassinfo-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumpluggableterminalclassinfo-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo">ITPluggableTerminalClassInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport2-enumeratepluggableterminalclasses">ITTerminalSupport2::EnumeratePluggableTerminalClasses</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/terminal-class">Terminal Class</a>
 

 


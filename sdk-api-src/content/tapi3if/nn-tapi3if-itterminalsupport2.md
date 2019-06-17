---
UID: NN:tapi3if.ITTerminalSupport2
title: ITTerminalSupport2 (tapi3if.h)
author: windows-sdk-content
description: The ITTerminalSupport2 interface is derived from the ITTerminalSupport interface. ITTerminalSupport2 supports the retrieval of information about pluggable terminal classes and superclasses by C, C++, and scripting applications.
old-location: tapi3\itterminalsupport2.htm
tech.root: Tapi
ms.assetid: 58611991-746c-4626-a1b1-535a2134ee27
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITTerminalSupport2, ITTerminalSupport2 interface [TAPI 2.2], ITTerminalSupport2 interface [TAPI 2.2],described, _tapi3_itterminalsupport2, tapi3.itterminalsupport2, tapi3if/ITTerminalSupport2
ms.topic: interface
f1_keywords: ["tapi3if/ITTerminalSupport2"]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITTerminalSupport2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITTerminalSupport2 interface


## -description


The 
<b>ITTerminalSupport2</b> interface is derived from the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport">ITTerminalSupport</a> interface. 
<b>ITTerminalSupport2</b> supports the retrieval of information about pluggable terminal classes and superclasses by C, C++, and scripting applications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTerminalSupport2</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITTerminalSupport2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITTerminalSupport2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport2-enumeratepluggablesuperclasses">EnumeratePluggableSuperclasses</a>
</td>
<td align="left" width="63%">
Gets an 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggablesuperclassinfo">IEnumPluggableSuperclassInfo</a> enumeration of pluggable terminal superclasses registered on the current system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport2-enumeratepluggableterminalclasses">EnumeratePluggableTerminalClasses</a>
</td>
<td align="left" width="63%">
Gets an 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggableterminalclassinfo">IEnumPluggableTerminalClassInfo</a> enumeration of the pluggable terminal classes registered under a given superclass.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport2-get_pluggablesuperclasses">get_PluggableSuperclasses</a>
</td>
<td align="left" width="63%">
Gets a collection of 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo">ITPluggableTerminalSuperclassInfo</a> superclass information interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport2-get_pluggableterminalclasses">get_PluggableTerminalClasses</a>
</td>
<td align="left" width="63%">
Gets a collection of 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo">ITPluggableTerminalClassInfo</a> terminal class information interfaces.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggablesuperclassinfo">IEnumPluggableSuperclassInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggableterminalclassinfo">IEnumPluggableTerminalClassInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo">ITPluggableTerminalClassInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo">ITPluggableTerminalSuperclassInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport">ITTerminalSupport</a>
 

 


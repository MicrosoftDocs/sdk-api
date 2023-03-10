---
UID: NN:tapi3if.ITPluggableTerminalSuperclassInfo
title: ITPluggableTerminalSuperclassInfo (tapi3if.h)
description: The ITPluggableTerminalSuperclassInfo interface exposes methods that get the name and CLSID of a pluggable terminal class.
helpviewer_keywords: ["ITPluggableTerminalSuperclassInfo","ITPluggableTerminalSuperclassInfo interface [TAPI 2.2]","ITPluggableTerminalSuperclassInfo interface [TAPI 2.2]","described","_tapi3_itpluggableterminalsuperclassinfo","tapi3.itpluggableterminalsuperclassinfo","tapi3if/ITPluggableTerminalSuperclassInfo"]
old-location: tapi3\itpluggableterminalsuperclassinfo.htm
tech.root: tapi3
ms.assetid: f9226af1-90e7-4317-af73-e1563883e2b6
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalSuperclassInfo, ITPluggableTerminalSuperclassInfo interface [TAPI 2.2], ITPluggableTerminalSuperclassInfo interface [TAPI 2.2],described, _tapi3_itpluggableterminalsuperclassinfo, tapi3.itpluggableterminalsuperclassinfo, tapi3if/ITPluggableTerminalSuperclassInfo
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
 - ITPluggableTerminalSuperclassInfo
 - tapi3if/ITPluggableTerminalSuperclassInfo
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
 - ITPluggableTerminalSuperclassInfo
---

# ITPluggableTerminalSuperclassInfo interface


## -description

The 
<b>ITPluggableTerminalSuperclassInfo</b> interface exposes methods that get the name and CLSID of a pluggable terminal class. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ienumpluggablesuperclassinfo-next">IEnumPluggableSuperclassInfo::Next</a> and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport2-get_pluggablesuperclasses">ITTerminalSupport2::get_PluggableSuperclasses</a> methods create the 
<b>ITPluggableTerminalSuperclassInfo</b> interface.

## -inheritance

The <b>ITPluggableTerminalSuperclassInfo</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITPluggableTerminalSuperclassInfo</b> also has these types of members:


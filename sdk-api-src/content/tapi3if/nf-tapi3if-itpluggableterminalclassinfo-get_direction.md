---
UID: NF:tapi3if.ITPluggableTerminalClassInfo.get_Direction
title: ITPluggableTerminalClassInfo::get_Direction (tapi3if.h)
description: The get_Direction method gets the direction supported by the terminal.
helpviewer_keywords: ["ITPluggableTerminalClassInfo interface [TAPI 2.2]","get_Direction method","ITPluggableTerminalClassInfo.get_Direction","ITPluggableTerminalClassInfo::get_Direction","_tapi3_itpluggableterminalclassinfo_get_direction","get_Direction","get_Direction method [TAPI 2.2]","get_Direction method [TAPI 2.2]","ITPluggableTerminalClassInfo interface","tapi3.itpluggableterminalclassinfo_get_direction","tapi3if/ITPluggableTerminalClassInfo::get_Direction"]
old-location: tapi3\itpluggableterminalclassinfo_get_direction.htm
tech.root: Tapi
ms.assetid: 843aeedc-08ca-436b-9d43-1e7b9aa1ac8e
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassInfo interface [TAPI 2.2],get_Direction method, ITPluggableTerminalClassInfo.get_Direction, ITPluggableTerminalClassInfo::get_Direction, _tapi3_itpluggableterminalclassinfo_get_direction, get_Direction, get_Direction method [TAPI 2.2], get_Direction method [TAPI 2.2],ITPluggableTerminalClassInfo interface, tapi3.itpluggableterminalclassinfo_get_direction, tapi3if/ITPluggableTerminalClassInfo::get_Direction
f1_keywords:
- tapi3if/ITPluggableTerminalClassInfo.get_Direction
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
- ITPluggableTerminalClassInfo.get_Direction
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPluggableTerminalClassInfo::get_Direction


## -description


The 
<b>get_Direction</b> method gets the direction supported by the terminal.


## -parameters




### -param pDirection [out]

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a> descriptor for the direction supported by the terminal.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo">ITPluggableTerminalClassInfo</a>
 

 


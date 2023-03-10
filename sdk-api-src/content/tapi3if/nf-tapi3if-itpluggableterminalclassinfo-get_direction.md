---
UID: NF:tapi3if.ITPluggableTerminalClassInfo.get_Direction
title: ITPluggableTerminalClassInfo::get_Direction (tapi3if.h)
description: The get_Direction method gets the direction supported by the terminal. (ITPluggableTerminalClassInfo.get_Direction)
helpviewer_keywords: ["ITPluggableTerminalClassInfo interface [TAPI 2.2]","get_Direction method","ITPluggableTerminalClassInfo.get_Direction","ITPluggableTerminalClassInfo::get_Direction","_tapi3_itpluggableterminalclassinfo_get_direction","get_Direction","get_Direction method [TAPI 2.2]","get_Direction method [TAPI 2.2]","ITPluggableTerminalClassInfo interface","tapi3.itpluggableterminalclassinfo_get_direction","tapi3if/ITPluggableTerminalClassInfo::get_Direction"]
old-location: tapi3\itpluggableterminalclassinfo_get_direction.htm
tech.root: tapi3
ms.assetid: 843aeedc-08ca-436b-9d43-1e7b9aa1ac8e
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassInfo interface [TAPI 2.2],get_Direction method, ITPluggableTerminalClassInfo.get_Direction, ITPluggableTerminalClassInfo::get_Direction, _tapi3_itpluggableterminalclassinfo_get_direction, get_Direction, get_Direction method [TAPI 2.2], get_Direction method [TAPI 2.2],ITPluggableTerminalClassInfo interface, tapi3.itpluggableterminalclassinfo_get_direction, tapi3if/ITPluggableTerminalClassInfo::get_Direction
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
 - ITPluggableTerminalClassInfo::get_Direction
 - tapi3if/ITPluggableTerminalClassInfo::get_Direction
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
 - ITPluggableTerminalClassInfo.get_Direction
---

# ITPluggableTerminalClassInfo::get_Direction


## -description

The 
<b>get_Direction</b> method gets the direction supported by the terminal.

## -parameters

### -param pDirection [out]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a> descriptor for the direction supported by the terminal.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo">ITPluggableTerminalClassInfo</a>

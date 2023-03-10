---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.put_Direction
title: ITPluggableTerminalClassRegistration::put_Direction (termmgr.h)
description: The put_Direction method sets the direction supported by the terminal.
helpviewer_keywords: ["ITPluggableTerminalClassRegistration interface [TAPI 2.2]","put_Direction method","ITPluggableTerminalClassRegistration.put_Direction","ITPluggableTerminalClassRegistration::put_Direction","_tapi3_itpluggableterminalclassregistration_put_direction","put_Direction","put_Direction method [TAPI 2.2]","put_Direction method [TAPI 2.2]","ITPluggableTerminalClassRegistration interface","tapi3.itpluggableterminalclassregistration_put_direction","termmgr/ITPluggableTerminalClassRegistration::put_Direction"]
old-location: tapi3\itpluggableterminalclassregistration_put_direction.htm
tech.root: tapi3
ms.assetid: b68c0697-e889-471d-857a-d11e974c6552
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],put_Direction method, ITPluggableTerminalClassRegistration.put_Direction, ITPluggableTerminalClassRegistration::put_Direction, _tapi3_itpluggableterminalclassregistration_put_direction, put_Direction, put_Direction method [TAPI 2.2], put_Direction method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_put_direction, termmgr/ITPluggableTerminalClassRegistration::put_Direction
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
 - ITPluggableTerminalClassRegistration::put_Direction
 - termmgr/ITPluggableTerminalClassRegistration::put_Direction
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
 - ITPluggableTerminalClassRegistration.put_Direction
---

# ITPluggableTerminalClassRegistration::put_Direction


## -description

The 
<b>put_Direction</b> method sets the direction supported by the terminal.

## -parameters

### -param nDirection [in]

The 
<a href="/windows/win32/api/termmgr/ne-termmgr-tmgr_direction">TMGR_DIRECTION</a> descriptor of the terminal direction.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>



<a href="/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-get_direction">get_Direction</a>
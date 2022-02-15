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

The <b>ITPluggableTerminalClassRegistration</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITPluggableTerminalClassRegistration</b> also has these types of members:


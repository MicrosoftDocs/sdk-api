---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.get_Direction
title: ITPluggableTerminalClassRegistration::get_Direction (termmgr.h)
author: windows-sdk-content
description: The get_Direction method gets the direction supported by the terminal.
old-location: tapi3\itpluggableterminalclassregistration_get_direction.htm
tech.root: Tapi
ms.assetid: 67f2f241-2389-476f-a412-af456c1c3376
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],get_Direction method, ITPluggableTerminalClassRegistration.get_Direction, ITPluggableTerminalClassRegistration::get_Direction, _tapi3_itpluggableterminalclassregistration_get_direction, get_Direction, get_Direction method [TAPI 2.2], get_Direction method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_get_direction, termmgr/ITPluggableTerminalClassRegistration::get_Direction
ms.topic: method
f1_keywords: 
 - "termmgr/ITPluggableTerminalClassRegistration.get_Direction"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPluggableTerminalClassRegistration.get_Direction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPluggableTerminalClassRegistration::get_Direction


## -description


The 
<b>get_Direction</b> method gets the direction supported by the terminal.


## -parameters




### -param pDirection [out]

The 
<a href="https://docs.microsoft.com/windows/win32/api/termmgr/ne-termmgr-tmgr_direction">TMGR_DIRECTION</a> descriptor of the terminal direction.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-put_direction">put_Direction</a>
 

 


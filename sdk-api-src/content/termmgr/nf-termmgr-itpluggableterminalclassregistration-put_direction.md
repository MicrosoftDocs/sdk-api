---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.put_Direction
title: ITPluggableTerminalClassRegistration::put_Direction
author: windows-sdk-content
description: The put_Direction method sets the direction supported by the terminal.
old-location: tapi3\itpluggableterminalclassregistration_put_direction.htm
tech.root: TAPI
ms.assetid: b68c0697-e889-471d-857a-d11e974c6552
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],put_Direction method, ITPluggableTerminalClassRegistration.put_Direction, ITPluggableTerminalClassRegistration::put_Direction, _tapi3_itpluggableterminalclassregistration_put_direction, put_Direction, put_Direction method [TAPI 2.2], put_Direction method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_put_direction, termmgr/ITPluggableTerminalClassRegistration::put_Direction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ITPluggableTerminalClassRegistration.put_Direction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPluggableTerminalClassRegistration::put_Direction


## -description


The 
<b>put_Direction</b> method sets the direction supported by the terminal.


## -parameters




### -param nDirection [in]

The 
<a href="https://msdn.microsoft.com/1758efb7-55fc-4925-be56-7f43177db64f">TMGR_DIRECTION</a> descriptor of the terminal direction.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/178824f5-9dda-4e8a-b921-f2c9d064a83c">ITPluggableTerminalClassRegistration</a>



<a href="https://msdn.microsoft.com/67f2f241-2389-476f-a412-af456c1c3376">get_Direction</a>
 

 


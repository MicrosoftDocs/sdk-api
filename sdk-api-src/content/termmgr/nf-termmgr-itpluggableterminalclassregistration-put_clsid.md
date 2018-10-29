---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.put_CLSID
title: ITPluggableTerminalClassRegistration::put_CLSID
author: windows-sdk-content
description: The put_CLSID method sets the CLSID used to CoCreateInstance the terminal.
old-location: tapi3\itpluggableterminalclassregistration_put_clsid.htm
tech.root: Tapi
ms.assetid: 9688cdc7-f55d-41c6-8db7-689617a24239
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],put_CLSID method, ITPluggableTerminalClassRegistration.put_CLSID, ITPluggableTerminalClassRegistration::put_CLSID, _tapi3_itpluggableterminalclassregistration_put_clsid, put_CLSID, put_CLSID method [TAPI 2.2], put_CLSID method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_put_clsid, termmgr/ITPluggableTerminalClassRegistration::put_CLSID
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
 - ITPluggableTerminalClassRegistration.put_CLSID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPluggableTerminalClassRegistration::put_CLSID


## -description


The 
<b>put_CLSID</b> method sets the CLSID used to <b>CoCreateInstance</b> the terminal.


## -parameters




### -param bstrCLSID [in]

The <b>BSTR</b> representation of the CLSID.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/178824f5-9dda-4e8a-b921-f2c9d064a83c">ITPluggableTerminalClassRegistration</a>



<a href="https://msdn.microsoft.com/085139b8-3f72-40d5-8323-c6083f06abe7">get_CLSID</a>
 

 


---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.get_MediaTypes
title: ITPluggableTerminalClassRegistration::get_MediaTypes
author: windows-sdk-content
description: The get_MediaTypes method gets the media types supported by the terminal.
old-location: tapi3\itpluggableterminalclassregistration_get_mediatypes.htm
tech.root: tapi
ms.assetid: aa8c0da8-2953-483a-b3b9-7a6f3e35c893
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],get_MediaTypes method, ITPluggableTerminalClassRegistration.get_MediaTypes, ITPluggableTerminalClassRegistration::get_MediaTypes, _tapi3_itpluggableterminalclassregistration_get_mediatypes, get_MediaTypes, get_MediaTypes method [TAPI 2.2], get_MediaTypes method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_get_mediatypes, termmgr/ITPluggableTerminalClassRegistration::get_MediaTypes
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
 - ITPluggableTerminalClassRegistration.get_MediaTypes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPluggableTerminalClassRegistration::get_MediaTypes


## -description


The 
<b>get_MediaTypes</b> method gets the media types supported by the terminal.


## -parameters




### -param pMediaTypes [out]

Bitwise ORed list of the 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media types</a> supported by the terminal.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/178824f5-9dda-4e8a-b921-f2c9d064a83c">ITPluggableTerminalClassRegistration</a>



<a href="https://msdn.microsoft.com/f5a5fb8b-5b71-4f57-8125-46c482897c21">put_MediaTypes</a>
 

 


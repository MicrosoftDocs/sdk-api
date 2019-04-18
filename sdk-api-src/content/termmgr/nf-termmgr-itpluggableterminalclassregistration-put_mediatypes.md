---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.put_MediaTypes
title: ITPluggableTerminalClassRegistration::put_MediaTypes (termmgr.h)
author: windows-sdk-content
description: The put_MediaTypes method sets the media types supported by the terminal.
old-location: tapi3\itpluggableterminalclassregistration_put_mediatypes.htm
tech.root: Tapi
ms.assetid: f5a5fb8b-5b71-4f57-8125-46c482897c21
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],put_MediaTypes method, ITPluggableTerminalClassRegistration.put_MediaTypes, ITPluggableTerminalClassRegistration::put_MediaTypes, _tapi3_itpluggableterminalclassregistration_put_mediatypes, put_MediaTypes, put_MediaTypes method [TAPI 2.2], put_MediaTypes method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_put_mediatypes, termmgr/ITPluggableTerminalClassRegistration::put_MediaTypes
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
 - ITPluggableTerminalClassRegistration.put_MediaTypes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPluggableTerminalClassRegistration::put_MediaTypes


## -description


The 
<b>put_MediaTypes</b> method sets the media types supported by the terminal.


## -parameters




### -param nMediaTypes [in]

Bitwise ORed list of the 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media types</a> supported by the terminal.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/178824f5-9dda-4e8a-b921-f2c9d064a83c">ITPluggableTerminalClassRegistration</a>



<a href="https://msdn.microsoft.com/aa8c0da8-2953-483a-b3b9-7a6f3e35c893">get_MediaTypes</a>
 

 


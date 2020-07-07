---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.get_MediaTypes
title: ITPluggableTerminalClassRegistration::get_MediaTypes (termmgr.h)
description: The get_MediaTypes method gets the media types supported by the terminal.
helpviewer_keywords: ["ITPluggableTerminalClassRegistration interface [TAPI 2.2]","get_MediaTypes method","ITPluggableTerminalClassRegistration.get_MediaTypes","ITPluggableTerminalClassRegistration::get_MediaTypes","_tapi3_itpluggableterminalclassregistration_get_mediatypes","get_MediaTypes","get_MediaTypes method [TAPI 2.2]","get_MediaTypes method [TAPI 2.2]","ITPluggableTerminalClassRegistration interface","tapi3.itpluggableterminalclassregistration_get_mediatypes","termmgr/ITPluggableTerminalClassRegistration::get_MediaTypes"]
old-location: tapi3\itpluggableterminalclassregistration_get_mediatypes.htm
tech.root: Tapi
ms.assetid: aa8c0da8-2953-483a-b3b9-7a6f3e35c893
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],get_MediaTypes method, ITPluggableTerminalClassRegistration.get_MediaTypes, ITPluggableTerminalClassRegistration::get_MediaTypes, _tapi3_itpluggableterminalclassregistration_get_mediatypes, get_MediaTypes, get_MediaTypes method [TAPI 2.2], get_MediaTypes method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_get_mediatypes, termmgr/ITPluggableTerminalClassRegistration::get_MediaTypes
f1_keywords:
- termmgr/ITPluggableTerminalClassRegistration.get_MediaTypes
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPluggableTerminalClassRegistration::get_MediaTypes


## -description


The 
<b>get_MediaTypes</b> method gets the media types supported by the terminal.


## -parameters




### -param pMediaTypes [out]

Bitwise ORed list of the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapimediatype--constants">media types</a> supported by the terminal.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-put_mediatypes">put_MediaTypes</a>
 

 


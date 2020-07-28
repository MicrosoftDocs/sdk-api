---
UID: NF:tapi3if.ITPluggableTerminalClassInfo.get_MediaTypes
title: ITPluggableTerminalClassInfo::get_MediaTypes (tapi3if.h)
description: The get_MediaTypes method gets the media types supported by the terminal.
helpviewer_keywords: ["ITPluggableTerminalClassInfo interface [TAPI 2.2]","get_MediaTypes method","ITPluggableTerminalClassInfo.get_MediaTypes","ITPluggableTerminalClassInfo::get_MediaTypes","_tapi3_itpluggableterminalclassinfo_get_mediatypes","get_MediaTypes","get_MediaTypes method [TAPI 2.2]","get_MediaTypes method [TAPI 2.2]","ITPluggableTerminalClassInfo interface","tapi3.itpluggableterminalclassinfo_get_mediatypes","tapi3if/ITPluggableTerminalClassInfo::get_MediaTypes"]
old-location: tapi3\itpluggableterminalclassinfo_get_mediatypes.htm
tech.root: tapi3
ms.assetid: 3c17540f-b899-4768-b0a2-2ab11f34636c
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassInfo interface [TAPI 2.2],get_MediaTypes method, ITPluggableTerminalClassInfo.get_MediaTypes, ITPluggableTerminalClassInfo::get_MediaTypes, _tapi3_itpluggableterminalclassinfo_get_mediatypes, get_MediaTypes, get_MediaTypes method [TAPI 2.2], get_MediaTypes method [TAPI 2.2],ITPluggableTerminalClassInfo interface, tapi3.itpluggableterminalclassinfo_get_mediatypes, tapi3if/ITPluggableTerminalClassInfo::get_MediaTypes
f1_keywords:
- tapi3if/ITPluggableTerminalClassInfo.get_MediaTypes
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
- ITPluggableTerminalClassInfo.get_MediaTypes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPluggableTerminalClassInfo::get_MediaTypes


## -description


The 
<b>get_MediaTypes</b> method gets the media types supported by the terminal.


## -parameters




### -param pMediaTypes [out]

 Bitwise ORed list of 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapimediatype--constants">media types</a> supported by the terminal.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo">ITPluggableTerminalClassInfo</a>
 

 


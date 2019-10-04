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
f1_keywords: 
 - "termmgr/ITPluggableTerminalClassRegistration.put_MediaTypes"
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
 - ITPluggableTerminalClassRegistration.put_MediaTypes
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
<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapimediatype--constants">media types</a> supported by the terminal.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-get_mediatypes">get_MediaTypes</a>
 

 


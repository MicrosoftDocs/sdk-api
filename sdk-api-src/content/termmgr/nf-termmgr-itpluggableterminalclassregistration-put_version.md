---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.put_Version
title: ITPluggableTerminalClassRegistration::put_Version (termmgr.h)
description: The put_Version method sets the terminal version.
helpviewer_keywords: ["ITPluggableTerminalClassRegistration interface [TAPI 2.2]","put_Version method","ITPluggableTerminalClassRegistration.put_Version","ITPluggableTerminalClassRegistration::put_Version","_tapi3_itpluggableterminalclassregistration_put_version","put_Version","put_Version method [TAPI 2.2]","put_Version method [TAPI 2.2]","ITPluggableTerminalClassRegistration interface","tapi3.itpluggableterminalclassregistration_put_version","termmgr/ITPluggableTerminalClassRegistration::put_Version"]
old-location: tapi3\itpluggableterminalclassregistration_put_version.htm
tech.root: tapi3
ms.assetid: 1fd659d3-869b-4055-bbd2-e567d13f239d
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],put_Version method, ITPluggableTerminalClassRegistration.put_Version, ITPluggableTerminalClassRegistration::put_Version, _tapi3_itpluggableterminalclassregistration_put_version, put_Version, put_Version method [TAPI 2.2], put_Version method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_put_version, termmgr/ITPluggableTerminalClassRegistration::put_Version
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
 - ITPluggableTerminalClassRegistration::put_Version
 - termmgr/ITPluggableTerminalClassRegistration::put_Version
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
 - ITPluggableTerminalClassRegistration.put_Version
---

# ITPluggableTerminalClassRegistration::put_Version


## -description

The 
<b>put_Version</b> method sets the terminal version.

## -parameters

### -param bstrVersion [in]

The <b>BSTR</b> representation of the terminal version.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>



<a href="/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-get_version">get_Version</a>
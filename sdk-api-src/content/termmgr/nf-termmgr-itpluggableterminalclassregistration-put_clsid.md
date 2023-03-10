---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.put_CLSID
title: ITPluggableTerminalClassRegistration::put_CLSID (termmgr.h)
description: The put_CLSID method sets the CLSID used to CoCreateInstance the terminal. (ITPluggableTerminalClassRegistration.put_CLSID)
helpviewer_keywords: ["ITPluggableTerminalClassRegistration interface [TAPI 2.2]","put_CLSID method","ITPluggableTerminalClassRegistration.put_CLSID","ITPluggableTerminalClassRegistration::put_CLSID","_tapi3_itpluggableterminalclassregistration_put_clsid","put_CLSID","put_CLSID method [TAPI 2.2]","put_CLSID method [TAPI 2.2]","ITPluggableTerminalClassRegistration interface","tapi3.itpluggableterminalclassregistration_put_clsid","termmgr/ITPluggableTerminalClassRegistration::put_CLSID"]
old-location: tapi3\itpluggableterminalclassregistration_put_clsid.htm
tech.root: tapi3
ms.assetid: 9688cdc7-f55d-41c6-8db7-689617a24239
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],put_CLSID method, ITPluggableTerminalClassRegistration.put_CLSID, ITPluggableTerminalClassRegistration::put_CLSID, _tapi3_itpluggableterminalclassregistration_put_clsid, put_CLSID, put_CLSID method [TAPI 2.2], put_CLSID method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_put_clsid, termmgr/ITPluggableTerminalClassRegistration::put_CLSID
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
 - ITPluggableTerminalClassRegistration::put_CLSID
 - termmgr/ITPluggableTerminalClassRegistration::put_CLSID
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
 - ITPluggableTerminalClassRegistration.put_CLSID
---

# ITPluggableTerminalClassRegistration::put_CLSID


## -description

The 
<b>put_CLSID</b> method sets the CLSID used to <b>CoCreateInstance</b> the terminal.

## -parameters

### -param bstrCLSID [in]

The <b>BSTR</b> representation of the CLSID.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>



<a href="/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-get_clsid">get_CLSID</a>

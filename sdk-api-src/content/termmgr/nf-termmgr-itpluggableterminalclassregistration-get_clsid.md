---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.get_CLSID
title: ITPluggableTerminalClassRegistration::get_CLSID (termmgr.h)
description: The get_CLSID method gets the CLSID used to CoCreateInstance the terminal.helpviewer_keywords: ["ITPluggableTerminalClassRegistration interface [TAPI 2.2]","get_CLSID method","ITPluggableTerminalClassRegistration.get_CLSID","ITPluggableTerminalClassRegistration::get_CLSID","_tapi3_itpluggableterminalclassregistration_get_clsid","get_CLSID","get_CLSID method [TAPI 2.2]","get_CLSID method [TAPI 2.2]","ITPluggableTerminalClassRegistration interface","tapi3.itpluggableterminalclassregistration_get_clsid","termmgr/ITPluggableTerminalClassRegistration::get_CLSID"]
old-location: tapi3\itpluggableterminalclassregistration_get_clsid.htm
tech.root: Tapi
ms.assetid: 085139b8-3f72-40d5-8323-c6083f06abe7
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],get_CLSID method, ITPluggableTerminalClassRegistration.get_CLSID, ITPluggableTerminalClassRegistration::get_CLSID, _tapi3_itpluggableterminalclassregistration_get_clsid, get_CLSID, get_CLSID method [TAPI 2.2], get_CLSID method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_get_clsid, termmgr/ITPluggableTerminalClassRegistration::get_CLSID
f1_keywords:
- termmgr/ITPluggableTerminalClassRegistration.get_CLSID
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
- ITPluggableTerminalClassRegistration.get_CLSID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPluggableTerminalClassRegistration::get_CLSID


## -description


The 
<b>get_CLSID</b> method gets the CLSID used to <b>CoCreateInstance</b> the terminal.


## -parameters




### -param pCLSID [out]

The <b>BSTR</b> representation of the CLSID. The <b>BSTR</b> is allocated using 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-put_clsid">put_CLSID</a>
 

 


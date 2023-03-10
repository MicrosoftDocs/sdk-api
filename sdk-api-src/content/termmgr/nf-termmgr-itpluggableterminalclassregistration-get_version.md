---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.get_Version
title: ITPluggableTerminalClassRegistration::get_Version (termmgr.h)
description: The get_Version method gets the terminal version. (ITPluggableTerminalClassRegistration.get_Version)
helpviewer_keywords: ["ITPluggableTerminalClassRegistration interface [TAPI 2.2]","get_Version method","ITPluggableTerminalClassRegistration.get_Version","ITPluggableTerminalClassRegistration::get_Version","_tapi3_itpluggableterminalclassregistration_get_version","get_Version","get_Version method [TAPI 2.2]","get_Version method [TAPI 2.2]","ITPluggableTerminalClassRegistration interface","tapi3.itpluggableterminalclassregistration_get_version","termmgr/ITPluggableTerminalClassRegistration::get_Version"]
old-location: tapi3\itpluggableterminalclassregistration_get_version.htm
tech.root: tapi3
ms.assetid: 2ce4345b-7d8e-4142-a4ee-df1e8b613a25
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],get_Version method, ITPluggableTerminalClassRegistration.get_Version, ITPluggableTerminalClassRegistration::get_Version, _tapi3_itpluggableterminalclassregistration_get_version, get_Version, get_Version method [TAPI 2.2], get_Version method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_get_version, termmgr/ITPluggableTerminalClassRegistration::get_Version
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
 - ITPluggableTerminalClassRegistration::get_Version
 - termmgr/ITPluggableTerminalClassRegistration::get_Version
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
 - ITPluggableTerminalClassRegistration.get_Version
---

# ITPluggableTerminalClassRegistration::get_Version


## -description

The 
<b>get_Version</b> method gets the terminal version.

## -parameters

### -param pVersion [out]

The <b>BSTR</b> representation of the terminal version. The <b>BSTR</b> is allocated using 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>



<a href="/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-put_version">put_Version</a>

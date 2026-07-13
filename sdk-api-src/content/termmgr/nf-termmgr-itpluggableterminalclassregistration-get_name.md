---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.get_Name
title: ITPluggableTerminalClassRegistration::get_Name (termmgr.h)
description: The get_Name method gets the terminal's friendly name. (ITPluggableTerminalClassRegistration.get_Name)
helpviewer_keywords: ["ITPluggableTerminalClassRegistration interface [TAPI 2.2]","get_Name method","ITPluggableTerminalClassRegistration.get_Name","ITPluggableTerminalClassRegistration::get_Name","_tapi3_itpluggableterminalclassregistration_get_name","get_Name","get_Name method [TAPI 2.2]","get_Name method [TAPI 2.2]","ITPluggableTerminalClassRegistration interface","tapi3.itpluggableterminalclassregistration_get_name","termmgr/ITPluggableTerminalClassRegistration::get_Name"]
old-location: tapi3\itpluggableterminalclassregistration_get_name.htm
tech.root: tapi3
ms.assetid: 0bbc0862-41d7-40cc-9b9d-57a2238122ee
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],get_Name method, ITPluggableTerminalClassRegistration.get_Name, ITPluggableTerminalClassRegistration::get_Name, _tapi3_itpluggableterminalclassregistration_get_name, get_Name, get_Name method [TAPI 2.2], get_Name method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_get_name, termmgr/ITPluggableTerminalClassRegistration::get_Name
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
 - ITPluggableTerminalClassRegistration::get_Name
 - termmgr/ITPluggableTerminalClassRegistration::get_Name
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
 - ITPluggableTerminalClassRegistration.get_Name
---

# ITPluggableTerminalClassRegistration::get_Name


## -description

The 
<b>get_Name</b> method gets the terminal's friendly name.

## -parameters

### -param pName [out]

The <b>BSTR</b> representation of the friendly name. The <b>BSTR</b> is allocated using 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>



<a href="/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-put_name">put_Name</a>

---
UID: NF:tapi3if.ITPluggableTerminalClassInfo.get_CLSID
title: ITPluggableTerminalClassInfo::get_CLSID (tapi3if.h)
description: The get_CLSID method gets the CLSID used to CoCreateInstance the terminal. (ITPluggableTerminalClassInfo.get_CLSID)
helpviewer_keywords: ["ITPluggableTerminalClassInfo interface [TAPI 2.2]","get_CLSID method","ITPluggableTerminalClassInfo.get_CLSID","ITPluggableTerminalClassInfo::get_CLSID","_tapi3_itpluggableterminalclassinfo_get_clsid","get_CLSID","get_CLSID method [TAPI 2.2]","get_CLSID method [TAPI 2.2]","ITPluggableTerminalClassInfo interface","tapi3.itpluggableterminalclassinfo_get_clsid","tapi3if/ITPluggableTerminalClassInfo::get_CLSID"]
old-location: tapi3\itpluggableterminalclassinfo_get_clsid.htm
tech.root: tapi3
ms.assetid: 17513c0f-bc3a-474b-a9e0-ea91e2ae7fbf
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassInfo interface [TAPI 2.2],get_CLSID method, ITPluggableTerminalClassInfo.get_CLSID, ITPluggableTerminalClassInfo::get_CLSID, _tapi3_itpluggableterminalclassinfo_get_clsid, get_CLSID, get_CLSID method [TAPI 2.2], get_CLSID method [TAPI 2.2],ITPluggableTerminalClassInfo interface, tapi3.itpluggableterminalclassinfo_get_clsid, tapi3if/ITPluggableTerminalClassInfo::get_CLSID
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITPluggableTerminalClassInfo::get_CLSID
 - tapi3if/ITPluggableTerminalClassInfo::get_CLSID
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
 - ITPluggableTerminalClassInfo.get_CLSID
---

# ITPluggableTerminalClassInfo::get_CLSID


## -description

The 
<b>get_CLSID</b> method gets the CLSID used to <b>CoCreateInstance</b> the terminal.

## -parameters

### -param pCLSID [out]

The <b>BSTR</b> representation of the CLSID. The <b>BSTR</b> is allocated using 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo">ITPluggableTerminalClassInfo</a>

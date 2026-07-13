---
UID: NF:tapi3if.ITPluggableTerminalClassInfo.get_Version
title: ITPluggableTerminalClassInfo::get_Version (tapi3if.h)
description: The get_Version method gets the terminal version. (ITPluggableTerminalClassInfo.get_Version)
helpviewer_keywords: ["ITPluggableTerminalClassInfo interface [TAPI 2.2]","get_Version method","ITPluggableTerminalClassInfo.get_Version","ITPluggableTerminalClassInfo::get_Version","_tapi3_itpluggableterminalclassinfo_get_version","get_Version","get_Version method [TAPI 2.2]","get_Version method [TAPI 2.2]","ITPluggableTerminalClassInfo interface","tapi3.itpluggableterminalclassinfo_get_version","tapi3if/ITPluggableTerminalClassInfo::get_Version"]
old-location: tapi3\itpluggableterminalclassinfo_get_version.htm
tech.root: tapi3
ms.assetid: e87ebf36-dace-4318-8d45-87f7a451284e
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassInfo interface [TAPI 2.2],get_Version method, ITPluggableTerminalClassInfo.get_Version, ITPluggableTerminalClassInfo::get_Version, _tapi3_itpluggableterminalclassinfo_get_version, get_Version, get_Version method [TAPI 2.2], get_Version method [TAPI 2.2],ITPluggableTerminalClassInfo interface, tapi3.itpluggableterminalclassinfo_get_version, tapi3if/ITPluggableTerminalClassInfo::get_Version
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
 - ITPluggableTerminalClassInfo::get_Version
 - tapi3if/ITPluggableTerminalClassInfo::get_Version
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
 - ITPluggableTerminalClassInfo.get_Version
---

# ITPluggableTerminalClassInfo::get_Version


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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo">ITPluggableTerminalClassInfo</a>

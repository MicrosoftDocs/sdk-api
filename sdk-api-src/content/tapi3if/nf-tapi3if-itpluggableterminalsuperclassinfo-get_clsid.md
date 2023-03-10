---
UID: NF:tapi3if.ITPluggableTerminalSuperclassInfo.get_CLSID
title: ITPluggableTerminalSuperclassInfo::get_CLSID (tapi3if.h)
description: The get_CLSID method gets the CLSID used to CoCreateInstance the terminal. (ITPluggableTerminalSuperclassInfo.get_CLSID)
helpviewer_keywords: ["ITPluggableTerminalSuperclassInfo interface [TAPI 2.2]","get_CLSID method","ITPluggableTerminalSuperclassInfo.get_CLSID","ITPluggableTerminalSuperclassInfo::get_CLSID","_tapi3_itpluggableterminalsuperclassinfo_get_clsid","get_CLSID","get_CLSID method [TAPI 2.2]","get_CLSID method [TAPI 2.2]","ITPluggableTerminalSuperclassInfo interface","tapi3.itpluggableterminalsuperclassinfo_get_clsid","tapi3if/ITPluggableTerminalSuperclassInfo::get_CLSID"]
old-location: tapi3\itpluggableterminalsuperclassinfo_get_clsid.htm
tech.root: tapi3
ms.assetid: 96f2fc11-43b0-4082-ab3d-d5813cd55ee2
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalSuperclassInfo interface [TAPI 2.2],get_CLSID method, ITPluggableTerminalSuperclassInfo.get_CLSID, ITPluggableTerminalSuperclassInfo::get_CLSID, _tapi3_itpluggableterminalsuperclassinfo_get_clsid, get_CLSID, get_CLSID method [TAPI 2.2], get_CLSID method [TAPI 2.2],ITPluggableTerminalSuperclassInfo interface, tapi3.itpluggableterminalsuperclassinfo_get_clsid, tapi3if/ITPluggableTerminalSuperclassInfo::get_CLSID
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
 - ITPluggableTerminalSuperclassInfo::get_CLSID
 - tapi3if/ITPluggableTerminalSuperclassInfo::get_CLSID
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
 - ITPluggableTerminalSuperclassInfo.get_CLSID
---

# ITPluggableTerminalSuperclassInfo::get_CLSID


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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo">ITPluggableTerminalSuperclassInfo</a>

---
UID: NF:tapi3if.ITPluggableTerminalSuperclassInfo.get_Name
title: ITPluggableTerminalSuperclassInfo::get_Name (tapi3if.h)
description: The get_Name method gets the terminal's friendly name. (ITPluggableTerminalSuperclassInfo.get_Name)
helpviewer_keywords: ["ITPluggableTerminalSuperclassInfo interface [TAPI 2.2]","get_Name method","ITPluggableTerminalSuperclassInfo.get_Name","ITPluggableTerminalSuperclassInfo::get_Name","_tapi3_itpluggableterminalsuperclassinfo_get_name","get_Name","get_Name method [TAPI 2.2]","get_Name method [TAPI 2.2]","ITPluggableTerminalSuperclassInfo interface","tapi3.itpluggableterminalsuperclassinfo_get_name","tapi3if/ITPluggableTerminalSuperclassInfo::get_Name"]
old-location: tapi3\itpluggableterminalsuperclassinfo_get_name.htm
tech.root: tapi3
ms.assetid: 36f1f8a9-5bde-43ea-a68a-15ea7d9415aa
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalSuperclassInfo interface [TAPI 2.2],get_Name method, ITPluggableTerminalSuperclassInfo.get_Name, ITPluggableTerminalSuperclassInfo::get_Name, _tapi3_itpluggableterminalsuperclassinfo_get_name, get_Name, get_Name method [TAPI 2.2], get_Name method [TAPI 2.2],ITPluggableTerminalSuperclassInfo interface, tapi3.itpluggableterminalsuperclassinfo_get_name, tapi3if/ITPluggableTerminalSuperclassInfo::get_Name
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
 - ITPluggableTerminalSuperclassInfo::get_Name
 - tapi3if/ITPluggableTerminalSuperclassInfo::get_Name
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
 - ITPluggableTerminalSuperclassInfo.get_Name
---

# ITPluggableTerminalSuperclassInfo::get_Name


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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo">ITPluggableTerminalSuperclassInfo</a>

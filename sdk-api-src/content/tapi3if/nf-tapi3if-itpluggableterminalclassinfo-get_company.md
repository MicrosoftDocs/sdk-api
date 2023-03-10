---
UID: NF:tapi3if.ITPluggableTerminalClassInfo.get_Company
title: ITPluggableTerminalClassInfo::get_Company (tapi3if.h)
description: The get_Company method gets the name of the company that issued this pluggable terminal. (ITPluggableTerminalClassInfo.get_Company)
helpviewer_keywords: ["ITPluggableTerminalClassInfo interface [TAPI 2.2]","get_Company method","ITPluggableTerminalClassInfo.get_Company","ITPluggableTerminalClassInfo::get_Company","_tapi3_itpluggableterminalclassinfo_get_company","get_Company","get_Company method [TAPI 2.2]","get_Company method [TAPI 2.2]","ITPluggableTerminalClassInfo interface","tapi3.itpluggableterminalclassinfo_get_company","tapi3if/ITPluggableTerminalClassInfo::get_Company"]
old-location: tapi3\itpluggableterminalclassinfo_get_company.htm
tech.root: tapi3
ms.assetid: b5595b18-264f-437f-8533-b7c87e6e7d00
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassInfo interface [TAPI 2.2],get_Company method, ITPluggableTerminalClassInfo.get_Company, ITPluggableTerminalClassInfo::get_Company, _tapi3_itpluggableterminalclassinfo_get_company, get_Company, get_Company method [TAPI 2.2], get_Company method [TAPI 2.2],ITPluggableTerminalClassInfo interface, tapi3.itpluggableterminalclassinfo_get_company, tapi3if/ITPluggableTerminalClassInfo::get_Company
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
 - ITPluggableTerminalClassInfo::get_Company
 - tapi3if/ITPluggableTerminalClassInfo::get_Company
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
 - ITPluggableTerminalClassInfo.get_Company
---

# ITPluggableTerminalClassInfo::get_Company


## -description

The 
<b>get_Company</b> method gets the name of the company that issued this pluggable terminal.

## -parameters

### -param pCompany [out]

The <b>BSTR</b> representation of the terminal's company name. The <b>BSTR</b> is allocated using 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo">ITPluggableTerminalClassInfo</a>

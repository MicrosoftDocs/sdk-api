---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.put_Company
title: ITPluggableTerminalClassRegistration::put_Company (termmgr.h)
description: The put_Company method sets the name of the company that issued this pluggable terminal.
helpviewer_keywords: ["ITPluggableTerminalClassRegistration interface [TAPI 2.2]","put_Company method","ITPluggableTerminalClassRegistration.put_Company","ITPluggableTerminalClassRegistration::put_Company","_tapi3_itpluggableterminalclassregistration_put_company","put_Company","put_Company method [TAPI 2.2]","put_Company method [TAPI 2.2]","ITPluggableTerminalClassRegistration interface","tapi3.itpluggableterminalclassregistration_put_company","termmgr/ITPluggableTerminalClassRegistration::put_Company"]
old-location: tapi3\itpluggableterminalclassregistration_put_company.htm
tech.root: tapi3
ms.assetid: e68539dc-0ebe-41f7-a9fe-941e2f941225
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],put_Company method, ITPluggableTerminalClassRegistration.put_Company, ITPluggableTerminalClassRegistration::put_Company, _tapi3_itpluggableterminalclassregistration_put_company, put_Company, put_Company method [TAPI 2.2], put_Company method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_put_company, termmgr/ITPluggableTerminalClassRegistration::put_Company
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
 - ITPluggableTerminalClassRegistration::put_Company
 - termmgr/ITPluggableTerminalClassRegistration::put_Company
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
 - ITPluggableTerminalClassRegistration.put_Company
---

# ITPluggableTerminalClassRegistration::put_Company


## -description

The 
<b>put_Company</b> method sets the name of the company that issued this pluggable terminal.

## -parameters

### -param bstrCompany [in]

The <b>BSTR</b> representation of the terminal's company name.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>



<a href="/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-get_company">get_Company</a>
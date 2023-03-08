---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.get_Company
title: ITPluggableTerminalClassRegistration::get_Company (termmgr.h)
description: The get_Company method gets the name of the company that issued this pluggable terminal. (ITPluggableTerminalClassRegistration.get_Company)
helpviewer_keywords: ["ITPluggableTerminalClassRegistration interface [TAPI 2.2]","get_Company method","ITPluggableTerminalClassRegistration.get_Company","ITPluggableTerminalClassRegistration::get_Company","_tapi3_itpluggableterminalclassregistration_get_company","get_Company","get_Company method [TAPI 2.2]","get_Company method [TAPI 2.2]","ITPluggableTerminalClassRegistration interface","tapi3.itpluggableterminalclassregistration_get_company","termmgr/ITPluggableTerminalClassRegistration::get_Company"]
old-location: tapi3\itpluggableterminalclassregistration_get_company.htm
tech.root: tapi3
ms.assetid: fea01c2a-e822-441a-89bc-8607762bc2eb
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],get_Company method, ITPluggableTerminalClassRegistration.get_Company, ITPluggableTerminalClassRegistration::get_Company, _tapi3_itpluggableterminalclassregistration_get_company, get_Company, get_Company method [TAPI 2.2], get_Company method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_get_company, termmgr/ITPluggableTerminalClassRegistration::get_Company
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
 - ITPluggableTerminalClassRegistration::get_Company
 - termmgr/ITPluggableTerminalClassRegistration::get_Company
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
 - ITPluggableTerminalClassRegistration.get_Company
---

# ITPluggableTerminalClassRegistration::get_Company


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

<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>



<a href="/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-put_company">put_Company</a>

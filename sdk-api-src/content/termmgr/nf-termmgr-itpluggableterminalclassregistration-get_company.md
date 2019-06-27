---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.get_Company
title: ITPluggableTerminalClassRegistration::get_Company (termmgr.h)
author: windows-sdk-content
description: The get_Company method gets the name of the company that issued this pluggable terminal.
old-location: tapi3\itpluggableterminalclassregistration_get_company.htm
tech.root: Tapi
ms.assetid: fea01c2a-e822-441a-89bc-8607762bc2eb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],get_Company method, ITPluggableTerminalClassRegistration.get_Company, ITPluggableTerminalClassRegistration::get_Company, _tapi3_itpluggableterminalclassregistration_get_company, get_Company, get_Company method [TAPI 2.2], get_Company method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_get_company, termmgr/ITPluggableTerminalClassRegistration::get_Company
ms.topic: method
f1_keywords: 
 - "termmgr/ITPluggableTerminalClassRegistration.get_Company"
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
 - ITPluggableTerminalClassRegistration.get_Company
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPluggableTerminalClassRegistration::get_Company


## -description


The 
<b>get_Company</b> method gets the name of the company that issued this pluggable terminal.


## -parameters




### -param pCompany [out]

The <b>BSTR</b> representation of the terminal's company name. The <b>BSTR</b> is allocated using 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-put_company">put_Company</a>
 

 


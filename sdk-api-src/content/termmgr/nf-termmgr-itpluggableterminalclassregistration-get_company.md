---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.get_Company
title: ITPluggableTerminalClassRegistration::get_Company
author: windows-sdk-content
description: The get_Company method gets the name of the company that issued this pluggable terminal.
old-location: tapi3\itpluggableterminalclassregistration_get_company.htm
tech.root: Tapi
ms.assetid: fea01c2a-e822-441a-89bc-8607762bc2eb
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],get_Company method, ITPluggableTerminalClassRegistration.get_Company, ITPluggableTerminalClassRegistration::get_Company, _tapi3_itpluggableterminalclassregistration_get_company, get_Company, get_Company method [TAPI 2.2], get_Company method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_get_company, termmgr/ITPluggableTerminalClassRegistration::get_Company
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# ITPluggableTerminalClassRegistration::get_Company


## -description


The 
<b>get_Company</b> method gets the name of the company that issued this pluggable terminal.


## -parameters




### -param pCompany [out]

The <b>BSTR</b> representation of the terminal's company name. The <b>BSTR</b> is allocated using 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/178824f5-9dda-4e8a-b921-f2c9d064a83c">ITPluggableTerminalClassRegistration</a>



<a href="https://msdn.microsoft.com/e68539dc-0ebe-41f7-a9fe-941e2f941225">put_Company</a>
 

 


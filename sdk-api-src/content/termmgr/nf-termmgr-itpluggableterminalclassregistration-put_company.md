---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.put_Company
title: ITPluggableTerminalClassRegistration::put_Company
author: windows-sdk-content
description: The put_Company method sets the name of the company that issued this pluggable terminal.
old-location: tapi3\itpluggableterminalclassregistration_put_company.htm
old-project: Tapi
ms.assetid: e68539dc-0ebe-41f7-a9fe-941e2f941225
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],put_Company method, ITPluggableTerminalClassRegistration.put_Company, ITPluggableTerminalClassRegistration::put_Company, _tapi3_itpluggableterminalclassregistration_put_company, put_Company, put_Company method [TAPI 2.2], put_Company method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_put_company, termmgr/ITPluggableTerminalClassRegistration::put_Company
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: TMGR_DIRECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITPluggableTerminalClassRegistration.put_Company
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPluggableTerminalClassRegistration::put_Company


## -description


The 
<b>put_Company</b> method sets the name of the company that issued this pluggable terminal.


## -parameters




### -param bstrCompany [in]

The <b>BSTR</b> representation of the terminal's company name.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/178824f5-9dda-4e8a-b921-f2c9d064a83c">ITPluggableTerminalClassRegistration</a>



<a href="https://msdn.microsoft.com/fea01c2a-e822-441a-89bc-8607762bc2eb">get_Company</a>
 

 


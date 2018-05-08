---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.GetTerminalClassInfo
title: ITPluggableTerminalClassRegistration::GetTerminalClassInfo
author: windows-driver-content
description: The GetTerminalClassInfo method gets all the information from the registry for a specific terminal.
old-location: tapi3\itpluggableterminalclassregistration_getterminalclassinfo.htm
old-project: Tapi
ms.assetid: 35eed68f-be15-4229-b1be-01734f1831c9
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: GetTerminalClassInfo, GetTerminalClassInfo method [TAPI 2.2], GetTerminalClassInfo method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, ITPluggableTerminalClassRegistration interface [TAPI 2.2],GetTerminalClassInfo method, ITPluggableTerminalClassRegistration.GetTerminalClassInfo, ITPluggableTerminalClassRegistration::GetTerminalClassInfo, _tapi3_itpluggableterminalclassregistration_getterminalclassinfo, tapi3.itpluggableterminalclassregistration_getterminalclassinfo, termmgr/ITPluggableTerminalClassRegistration::GetTerminalClassInfo
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
req.typenames: TMGR_DIRECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITPluggableTerminalClassRegistration.GetTerminalClassInfo
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPluggableTerminalClassRegistration::GetTerminalClassInfo


## -description


The 
<b>GetTerminalClassInfo</b> method gets all the information from the registry for a specific terminal.


## -parameters




### -param bstrSuperclass [in]

The <b>BSTR</b> representation of the CLSID for the terminal superclass.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/178824f5-9dda-4e8a-b921-f2c9d064a83c">ITPluggableTerminalClassRegistration</a>
 

 


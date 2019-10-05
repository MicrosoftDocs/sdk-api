---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.GetTerminalClassInfo
title: ITPluggableTerminalClassRegistration::GetTerminalClassInfo (termmgr.h)
author: windows-sdk-content
description: The GetTerminalClassInfo method gets all the information from the registry for a specific terminal.
old-location: tapi3\itpluggableterminalclassregistration_getterminalclassinfo.htm
tech.root: Tapi
ms.assetid: 35eed68f-be15-4229-b1be-01734f1831c9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTerminalClassInfo, GetTerminalClassInfo method [TAPI 2.2], GetTerminalClassInfo method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, ITPluggableTerminalClassRegistration interface [TAPI 2.2],GetTerminalClassInfo method, ITPluggableTerminalClassRegistration.GetTerminalClassInfo, ITPluggableTerminalClassRegistration::GetTerminalClassInfo, _tapi3_itpluggableterminalclassregistration_getterminalclassinfo, tapi3.itpluggableterminalclassregistration_getterminalclassinfo, termmgr/ITPluggableTerminalClassRegistration::GetTerminalClassInfo
ms.topic: method
f1_keywords: 
 - "termmgr/ITPluggableTerminalClassRegistration.GetTerminalClassInfo"
dev_langs:
 - c++
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
 - ITPluggableTerminalClassRegistration.GetTerminalClassInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>
 

 


---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.GetTerminalClassInfo
title: ITPluggableTerminalClassRegistration::GetTerminalClassInfo (termmgr.h)
description: The GetTerminalClassInfo method gets all the information from the registry for a specific terminal.
helpviewer_keywords: ["GetTerminalClassInfo","GetTerminalClassInfo method [TAPI 2.2]","GetTerminalClassInfo method [TAPI 2.2]","ITPluggableTerminalClassRegistration interface","ITPluggableTerminalClassRegistration interface [TAPI 2.2]","GetTerminalClassInfo method","ITPluggableTerminalClassRegistration.GetTerminalClassInfo","ITPluggableTerminalClassRegistration::GetTerminalClassInfo","_tapi3_itpluggableterminalclassregistration_getterminalclassinfo","tapi3.itpluggableterminalclassregistration_getterminalclassinfo","termmgr/ITPluggableTerminalClassRegistration::GetTerminalClassInfo"]
old-location: tapi3\itpluggableterminalclassregistration_getterminalclassinfo.htm
tech.root: tapi3
ms.assetid: 35eed68f-be15-4229-b1be-01734f1831c9
ms.date: 12/05/2018
ms.keywords: GetTerminalClassInfo, GetTerminalClassInfo method [TAPI 2.2], GetTerminalClassInfo method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, ITPluggableTerminalClassRegistration interface [TAPI 2.2],GetTerminalClassInfo method, ITPluggableTerminalClassRegistration.GetTerminalClassInfo, ITPluggableTerminalClassRegistration::GetTerminalClassInfo, _tapi3_itpluggableterminalclassregistration_getterminalclassinfo, tapi3.itpluggableterminalclassregistration_getterminalclassinfo, termmgr/ITPluggableTerminalClassRegistration::GetTerminalClassInfo
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
 - ITPluggableTerminalClassRegistration::GetTerminalClassInfo
 - termmgr/ITPluggableTerminalClassRegistration::GetTerminalClassInfo
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
 - ITPluggableTerminalClassRegistration.GetTerminalClassInfo
---

# ITPluggableTerminalClassRegistration::GetTerminalClassInfo


## -description

The 
<b>GetTerminalClassInfo</b> method gets all the information from the registry for a specific terminal.

## -parameters

### -param bstrSuperclass [in]

The <b>BSTR</b> representation of the CLSID for the terminal superclass.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>
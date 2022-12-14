---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.put_Name
title: ITPluggableTerminalClassRegistration::put_Name (termmgr.h)
description: The put_Name method sets the name of the terminal class being registered.
helpviewer_keywords: ["ITPluggableTerminalClassRegistration interface [TAPI 2.2]","put_Name method","ITPluggableTerminalClassRegistration.put_Name","ITPluggableTerminalClassRegistration::put_Name","_tapi3_itpluggableterminalclassregistration_put_name","put_Name","put_Name method [TAPI 2.2]","put_Name method [TAPI 2.2]","ITPluggableTerminalClassRegistration interface","tapi3.itpluggableterminalclassregistration_put_name","termmgr/ITPluggableTerminalClassRegistration::put_Name"]
old-location: tapi3\itpluggableterminalclassregistration_put_name.htm
tech.root: tapi3
ms.assetid: d3d6c585-5592-4ed9-80bb-a55ff151edd1
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],put_Name method, ITPluggableTerminalClassRegistration.put_Name, ITPluggableTerminalClassRegistration::put_Name, _tapi3_itpluggableterminalclassregistration_put_name, put_Name, put_Name method [TAPI 2.2], put_Name method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_put_name, termmgr/ITPluggableTerminalClassRegistration::put_Name
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
 - ITPluggableTerminalClassRegistration::put_Name
 - termmgr/ITPluggableTerminalClassRegistration::put_Name
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
 - ITPluggableTerminalClassRegistration.put_Name
---

# ITPluggableTerminalClassRegistration::put_Name


## -description

The 
<b>put_Name</b> method sets the name of the terminal class being registered.

## -parameters

### -param bstrName [in]

The <b>BSTR</b> representation of the name.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>



<a href="/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-get_name">get_Name</a>
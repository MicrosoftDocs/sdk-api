---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.Add
title: ITPluggableTerminalClassRegistration::Add (termmgr.h)
description: The Add method adds terminal information to the registry. If an entry for the terminal already exists, the method edits the entry.
helpviewer_keywords: ["Add","Add method [TAPI 2.2]","Add method [TAPI 2.2]","ITPluggableTerminalClassRegistration interface","ITPluggableTerminalClassRegistration interface [TAPI 2.2]","Add method","ITPluggableTerminalClassRegistration.Add","ITPluggableTerminalClassRegistration::Add","_tapi3_itpluggableterminalclassregistration_add","tapi3.itpluggableterminalclassregistration_add","termmgr/ITPluggableTerminalClassRegistration::Add"]
old-location: tapi3\itpluggableterminalclassregistration_add.htm
tech.root: tapi3
ms.assetid: 2e5104e1-5276-4c5b-9a1a-404904432982
ms.date: 12/05/2018
ms.keywords: Add, Add method [TAPI 2.2], Add method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, ITPluggableTerminalClassRegistration interface [TAPI 2.2],Add method, ITPluggableTerminalClassRegistration.Add, ITPluggableTerminalClassRegistration::Add, _tapi3_itpluggableterminalclassregistration_add, tapi3.itpluggableterminalclassregistration_add, termmgr/ITPluggableTerminalClassRegistration::Add
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
 - ITPluggableTerminalClassRegistration::Add
 - termmgr/ITPluggableTerminalClassRegistration::Add
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
 - ITPluggableTerminalClassRegistration.Add
---

# ITPluggableTerminalClassRegistration::Add


## -description

The 
<b>Add</b> method adds terminal information to the registry. If an entry for the terminal already exists, the method edits the entry.

## -parameters

### -param bstrSuperclass [in]

The <b>BSTR</b> representation of the CLSID for the terminal superclass.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-delete">Delete</a>



<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>
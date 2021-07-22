---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.put_TerminalClass
title: ITPluggableTerminalClassRegistration::put_TerminalClass (termmgr.h)
description: The put_TerminalClass method sets the terminal's terminal class.
helpviewer_keywords: ["ITPluggableTerminalClassRegistration interface [TAPI 2.2]","put_TerminalClass method","ITPluggableTerminalClassRegistration.put_TerminalClass","ITPluggableTerminalClassRegistration::put_TerminalClass","_tapi3_itpluggableterminalclassregistration_put_terminalclass","put_TerminalClass","put_TerminalClass method [TAPI 2.2]","put_TerminalClass method [TAPI 2.2]","ITPluggableTerminalClassRegistration interface","tapi3.itpluggableterminalclassregistration_put_terminalclass","termmgr/ITPluggableTerminalClassRegistration::put_TerminalClass"]
old-location: tapi3\itpluggableterminalclassregistration_put_terminalclass.htm
tech.root: tapi3
ms.assetid: 257adef8-f578-4c8c-9fe9-df59572b7f6e
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],put_TerminalClass method, ITPluggableTerminalClassRegistration.put_TerminalClass, ITPluggableTerminalClassRegistration::put_TerminalClass, _tapi3_itpluggableterminalclassregistration_put_terminalclass, put_TerminalClass, put_TerminalClass method [TAPI 2.2], put_TerminalClass method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_put_terminalclass, termmgr/ITPluggableTerminalClassRegistration::put_TerminalClass
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
 - ITPluggableTerminalClassRegistration::put_TerminalClass
 - termmgr/ITPluggableTerminalClassRegistration::put_TerminalClass
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
 - ITPluggableTerminalClassRegistration.put_TerminalClass
---

# ITPluggableTerminalClassRegistration::put_TerminalClass


## -description

The 
<b>put_TerminalClass</b> method sets the terminal's terminal class.

## -parameters

### -param bstrTerminalClass [in]

The <b>BSTR</b> representation of the 
<a href="/windows/desktop/Tapi/terminal-class">terminal class</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>



<a href="/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-get_terminalclass">get_TerminalClass</a>
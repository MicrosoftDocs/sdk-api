---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.get_TerminalClass
title: ITPluggableTerminalClassRegistration::get_TerminalClass (termmgr.h)
description: The get_TerminalClass method gets the terminal's terminal class.
old-location: tapi3\itpluggableterminalclassregistration_get_terminalclass.htm
tech.root: Tapi
ms.assetid: 8da33c46-a369-4501-8249-48ad5d454c58
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassRegistration interface [TAPI 2.2],get_TerminalClass method, ITPluggableTerminalClassRegistration.get_TerminalClass, ITPluggableTerminalClassRegistration::get_TerminalClass, _tapi3_itpluggableterminalclassregistration_get_terminalclass, get_TerminalClass, get_TerminalClass method [TAPI 2.2], get_TerminalClass method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, tapi3.itpluggableterminalclassregistration_get_terminalclass, termmgr/ITPluggableTerminalClassRegistration::get_TerminalClass
ms.topic: method
f1_keywords:
- termmgr/ITPluggableTerminalClassRegistration.get_TerminalClass
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
- ITPluggableTerminalClassRegistration.get_TerminalClass
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPluggableTerminalClassRegistration::get_TerminalClass


## -description


The 
<b>get_TerminalClass</b> method gets the terminal's terminal class.


## -parameters




### -param pTerminalClass [out]

The <b>BSTR</b> representation of the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/terminal-class">terminal class</a>. The <b>BSTR</b> is allocated using 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-put_terminalclass">put_TerminalClass</a>
 

 


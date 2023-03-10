---
UID: NF:tapi3if.ITPluggableTerminalClassInfo.get_TerminalClass
title: ITPluggableTerminalClassInfo::get_TerminalClass (tapi3if.h)
description: The get_TerminalClass method gets the terminal's terminal class. (ITPluggableTerminalClassInfo.get_TerminalClass)
helpviewer_keywords: ["ITPluggableTerminalClassInfo interface [TAPI 2.2]","get_TerminalClass method","ITPluggableTerminalClassInfo.get_TerminalClass","ITPluggableTerminalClassInfo::get_TerminalClass","_tapi3_itpluggableterminalclassinfo_get_terminalclass","get_TerminalClass","get_TerminalClass method [TAPI 2.2]","get_TerminalClass method [TAPI 2.2]","ITPluggableTerminalClassInfo interface","tapi3.itpluggableterminalclassinfo_get_terminalclass","tapi3if/ITPluggableTerminalClassInfo::get_TerminalClass"]
old-location: tapi3\itpluggableterminalclassinfo_get_terminalclass.htm
tech.root: tapi3
ms.assetid: 7dfa6cf8-23b8-4959-ba39-6efda1d71562
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalClassInfo interface [TAPI 2.2],get_TerminalClass method, ITPluggableTerminalClassInfo.get_TerminalClass, ITPluggableTerminalClassInfo::get_TerminalClass, _tapi3_itpluggableterminalclassinfo_get_terminalclass, get_TerminalClass, get_TerminalClass method [TAPI 2.2], get_TerminalClass method [TAPI 2.2],ITPluggableTerminalClassInfo interface, tapi3.itpluggableterminalclassinfo_get_terminalclass, tapi3if/ITPluggableTerminalClassInfo::get_TerminalClass
req.header: tapi3if.h
req.include-header: Tapi3.h
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
 - ITPluggableTerminalClassInfo::get_TerminalClass
 - tapi3if/ITPluggableTerminalClassInfo::get_TerminalClass
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
 - ITPluggableTerminalClassInfo.get_TerminalClass
---

# ITPluggableTerminalClassInfo::get_TerminalClass


## -description

The 
<b>get_TerminalClass</b> method gets the terminal's terminal class.

## -parameters

### -param pTerminalClass [out]

 The <b>BSTR</b> representation of the terminal's 
<a href="/windows/desktop/Tapi/terminal-class">terminal class</a>. The <b>BSTR</b> is allocated using 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. It should be deallocated by the client.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo">ITPluggableTerminalClassInfo</a>

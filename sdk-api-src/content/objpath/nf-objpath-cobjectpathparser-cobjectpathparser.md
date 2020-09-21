---
UID: NF:objpath.CObjectPathParser.CObjectPathParser
title: CObjectPathParser::CObjectPathParser (objpath.h)
description: Constructs and initializes an instance of a CObjectPathParser object that requires a full object path. Use of this object is not recommended. Instead, use the IWbemPath COM interface.
helpviewer_keywords: ["??0CObjectPathParser@@QAE@W4ObjectParserFlags@@@Z","??0CObjectPathParser@@QEAA@W4ObjectParserFlags@@@Z","CObjectPathParser","CObjectPathParser interface [Windows Management Instrumentation]","CObjectPathParser method","CObjectPathParser method [Windows Management Instrumentation]","CObjectPathParser method [Windows Management Instrumentation]","CObjectPathParser interface","CObjectPathParser.CObjectPathParser","CObjectPathParser::CObjectPathParser","objpath/CObjectPathParser::CObjectPathParser","wmi.cobjectpathparser_cobjectpathparser"]
old-location: wmi\cobjectpathparser_cobjectpathparser.htm
tech.root: wmi
ms.assetid: 8aeb162a-8e93-4a2f-9609-693a26027a44
ms.date: 12/05/2018
ms.keywords: ??0CObjectPathParser@@QAE@W4ObjectParserFlags@@@Z, ??0CObjectPathParser@@QEAA@W4ObjectParserFlags@@@Z, CObjectPathParser, CObjectPathParser interface [Windows Management Instrumentation],CObjectPathParser method, CObjectPathParser method [Windows Management Instrumentation], CObjectPathParser method [Windows Management Instrumentation],CObjectPathParser interface, CObjectPathParser.CObjectPathParser, CObjectPathParser::CObjectPathParser, objpath/CObjectPathParser::CObjectPathParser, wmi.cobjectpathparser_cobjectpathparser
req.header: objpath.h
req.include-header: ObjPath.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CObjectPathParser::CObjectPathParser
 - objpath/CObjectPathParser::CObjectPathParser
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CObjectPathParser.CObjectPathParser
 - ??0CObjectPathParser@@QAE@W4ObjectParserFlags@@@Z
 - ??0CObjectPathParser@@QEAA@W4ObjectParserFlags@@@Z
---

# CObjectPathParser::CObjectPathParser


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/objpath/nl-objpath-cobjectpathparser">CObjectPathParser</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

Constructs and initializes an instance of a <a href="/windows/desktop/api/objpath/nl-objpath-cobjectpathparser">CObjectPathParser</a> object that requires a full object path. Use of  this object is not recommended. Instead, use the <a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a> COM interface.

## -parameters

### -param eFlags [in]

One of the flags from the <a href="/windows/desktop/api/objpath/ne-objpath-objectparserflags">ObjectParserFlags</a> enumeration.

## -see-also

<a href="/windows/desktop/api/objpath/nl-objpath-cobjectpathparser">CObjectPathParser</a>
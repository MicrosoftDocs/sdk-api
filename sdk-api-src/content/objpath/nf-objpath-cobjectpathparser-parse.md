---
UID: NF:objpath.CObjectPathParser.Parse
title: CObjectPathParser::Parse (objpath.h)
description: Parses a string that contains a WMI path into a structure the contains the path parts, such as the server, namespace, class, key that identifies an instance, and others. Use of this object is not recommended. Instead, use the IWbemPath COM interface.
helpviewer_keywords: ["?Parse@CObjectPathParser@@QAEHPBGPAPAUParsedObjectPath@@@Z","?Parse@CObjectPathParser@@QEAAHPEBGPEAPEAUParsedObjectPath@@@Z","CObjectPathParser interface [Windows Management Instrumentation]","Parse method","CObjectPathParser.Parse","CObjectPathParser::Parse","Parse","Parse method [Windows Management Instrumentation]","Parse method [Windows Management Instrumentation]","CObjectPathParser interface","objpath/CObjectPathParser::Parse","wmi.cobjectpathparser_parse"]
old-location: wmi\cobjectpathparser_parse.htm
tech.root: wmi
ms.assetid: c39dbef5-9050-487a-8e06-17087753330d
ms.date: 12/05/2018
ms.keywords: ?Parse@CObjectPathParser@@QAEHPBGPAPAUParsedObjectPath@@@Z, ?Parse@CObjectPathParser@@QEAAHPEBGPEAPEAUParsedObjectPath@@@Z, CObjectPathParser interface [Windows Management Instrumentation],Parse method, CObjectPathParser.Parse, CObjectPathParser::Parse, Parse, Parse method [Windows Management Instrumentation], Parse method [Windows Management Instrumentation],CObjectPathParser interface, objpath/CObjectPathParser::Parse, wmi.cobjectpathparser_parse
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
 - CObjectPathParser::Parse
 - objpath/CObjectPathParser::Parse
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
 - CObjectPathParser.Parse
 - ?Parse@CObjectPathParser@@QAEHPBGPAPAUParsedObjectPath@@@Z
 - ?Parse@CObjectPathParser@@QEAAHPEBGPEAPEAUParsedObjectPath@@@Z
---

# CObjectPathParser::Parse


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/objpath/nl-objpath-cobjectpathparser">CObjectPathParser</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

Parses a string that contains a WMI path into a structure the contains the path parts, such as the server, namespace, class, key that identifies an instance, and others. Use of  this object is not recommended. Instead, use the <a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a> COM interface.

## -parameters

### -param RawPath [in]

The raw path data.

### -param pOutput [out]

A structure that contains the parsed path parts.

## -see-also

<a href="/windows/desktop/api/objpath/nl-objpath-cobjectpathparser">CObjectPathParser</a>
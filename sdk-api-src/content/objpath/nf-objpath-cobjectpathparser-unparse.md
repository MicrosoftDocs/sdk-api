---
UID: NF:objpath.CObjectPathParser.Unparse
title: CObjectPathParser::Unparse (objpath.h)
description: Converts a structure that contains the parsed path to a string. Use of this object is not recommended. Instead, use the IWbemPath COM interface.
helpviewer_keywords: ["CObjectPathParser interface [Windows Management Instrumentation]","UnParse method","CObjectPathParser.Unparse","CObjectPathParser::UnParse","CObjectPathParser::Unparse","UnParse method [Windows Management Instrumentation]","UnParse method [Windows Management Instrumentation]","CObjectPathParser interface","Unparse","objpath/CObjectPathParser::UnParse","wmi.cobjectpathparser_unparse"]
old-location: wmi\cobjectpathparser_unparse.htm
tech.root: wmi
ms.assetid: 6135b808-b9eb-4ba0-9eb8-e7a59993ae34
ms.date: 12/05/2018
ms.keywords: CObjectPathParser interface [Windows Management Instrumentation],UnParse method, CObjectPathParser.Unparse, CObjectPathParser::UnParse, CObjectPathParser::Unparse, UnParse method [Windows Management Instrumentation], UnParse method [Windows Management Instrumentation],CObjectPathParser interface, Unparse, objpath/CObjectPathParser::UnParse, wmi.cobjectpathparser_unparse
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
 - CObjectPathParser::Unparse
 - objpath/CObjectPathParser::Unparse
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CObjectPathParser.UnParse
---

# CObjectPathParser::Unparse


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/objpath/nl-objpath-cobjectpathparser">CObjectPathParser</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

Converts a structure that contains the parsed path to a string. Use of  this object is not recommended. Instead, use the <a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a> COM interface.

## -parameters

### -param pInput [in]

A structure that contains WMI path parts such as server, namespaces, classes, key value identifying a specific instance, and others.

### -param pwszPath [out]

A structure that contains the WMI path.

## -remarks

<b>UnParse</b> is a static method.

## -see-also

<a href="/windows/desktop/api/objpath/nl-objpath-cobjectpathparser">CObjectPathParser</a>
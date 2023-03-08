---
UID: NF:objpath.CObjectPathParser.Free(LPWSTR)
title: CObjectPathParser::Free(LPWSTR) (objpath.h)
description: Releases the memory that contains the unparsed path. Use of this object is not recommended. Instead, use the IWbemPath COM interface. (overload 2/2)
helpviewer_keywords: ["CObjectPathParser interface [Windows Management Instrumentation]","Free method","CObjectPathParser.Free","CObjectPathParser.Free(LPWSTR)","CObjectPathParser::Free","CObjectPathParser::Free(LPWSTR)","Free","Free method [Windows Management Instrumentation]","Free method [Windows Management Instrumentation]","CObjectPathParser interface","objpath/CObjectPathParser::Free","wmi.cobjectpathparser_free_lpwstr_"]
old-location: wmi\cobjectpathparser_free_lpwstr_.htm
tech.root: wmi
ms.assetid: 3a18a29a-269a-490c-8ede-6ec6b77f99f7
ms.date: 12/05/2018
ms.keywords: CObjectPathParser interface [Windows Management Instrumentation],Free method, CObjectPathParser.Free, CObjectPathParser.Free(LPWSTR), CObjectPathParser::Free, CObjectPathParser::Free(LPWSTR), Free, Free method [Windows Management Instrumentation], Free method [Windows Management Instrumentation],CObjectPathParser interface, objpath/CObjectPathParser::Free, wmi.cobjectpathparser_free_lpwstr_
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
 - CObjectPathParser::Free
 - objpath/CObjectPathParser::Free
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
 - CObjectPathParser.Free
---

# CObjectPathParser::Free(LPWSTR)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/objpath/nl-objpath-cobjectpathparser">CObjectPathParser</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

Releases the memory that contains the unparsed path.  Use of  this object is not recommended. Instead, use the <a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a> COM interface.

## -parameters

### -param wszUnparsedPath

Memory containing the unparsed path information.




## -see-also

<a href="/windows/desktop/api/objpath/nl-objpath-cobjectpathparser">CObjectPathParser</a>

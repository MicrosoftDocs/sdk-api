---
UID: NS:wbemcli.tag_CompileStatusInfo
title: WBEM_COMPILE_STATUS_INFO (wbemcli.h)
description: Describes an error for the IMofCompiler interface.
helpviewer_keywords: ["WBEM_COMPILE_STATUS_INFO","WBEM_COMPILE_STATUS_INFO structure [Windows Management Instrumentation]","wbemcli/tag_CompileStatusInfo","wmi.wbem_compile_status_info"]
old-location: wmi\wbem_compile_status_info.htm
tech.root: wmi
ms.assetid: 94B3516F-2DDA-4C93-B48E-67D7FE357F4E
ms.date: 12/05/2018
ms.keywords: WBEM_COMPILE_STATUS_INFO, WBEM_COMPILE_STATUS_INFO structure [Windows Management Instrumentation], wbemcli/tag_CompileStatusInfo, wmi.wbem_compile_status_info
req.header: wbemcli.h
req.include-header: Wbemidl.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WBEM_COMPILE_STATUS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_CompileStatusInfo
 - wbemcli/tag_CompileStatusInfo
 - WBEM_COMPILE_STATUS_INFO
 - wbemcli/WBEM_COMPILE_STATUS_INFO
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - WBEM_COMPILE_STATUS_INFO
---

# WBEM_COMPILE_STATUS_INFO structure


## -description

Describes an error for the <a href="/windows/desktop/api/wbemcli/nn-wbemcli-imofcompiler">IMofCompiler</a> interface.

## -struct-fields

### -field lPhaseError

TBD



#### 0

no error



#### 1

parsing error



#### 2

argument error



#### 3

errors occurred while storing the data.

### -field hRes

The actual error code.

### -field ObjectNum

Object that is at fault.

### -field FirstLine

First line number of the object.

### -field LastLine

Last line number of the object.

### -field dwOutFlags

Reserved.

## -remarks

The   <i>ObjectNum</i>, <i>FirstLine</i>, and <i>LastLine</i> parameters only contain values for errors that relate to a particular class or instance in the file.

## -see-also

<a href="/windows/desktop/api/wbemcli/nf-wbemcli-imofcompiler-compilebuffer">CompileBuffer</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-imofcompiler-compilefile">CompileFile</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-imofcompiler-createbmof">CreateBMOF</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-imofcompiler">IMofCompiler</a>
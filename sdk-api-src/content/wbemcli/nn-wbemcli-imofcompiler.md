---
UID: NN:wbemcli.IMofCompiler
title: IMofCompiler (wbemcli.h)
description: The IMofCompiler interface, implemented by Mofd.dll, provides a COM interface that is used by the Managed Object Format (MOF) compiler and any other applications that compile MOF files.
helpviewer_keywords: ["IMofCompiler","IMofCompiler interface [Windows Management Instrumentation]","IMofCompiler interface [Windows Management Instrumentation]","described","MofCompiler","_hmm_imofcompiler","wbemcli/IMofCompiler","wmi.imofcompiler"]
old-location: wmi\imofcompiler.htm
tech.root: wmi
ms.assetid: 5e01c7ac-7090-4cde-b836-01fa9d3f27f5
ms.date: 12/05/2018
ms.keywords: IMofCompiler, IMofCompiler interface [Windows Management Instrumentation], IMofCompiler interface [Windows Management Instrumentation],described, MofCompiler, _hmm_imofcompiler, wbemcli/IMofCompiler, wmi.imofcompiler
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
req.lib: Wbemuuid.lib
req.dll: Mofd.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMofCompiler
 - wbemcli/IMofCompiler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mofd.dll
api_name:
 - IMofCompiler
 - MofCompiler
---

# IMofCompiler interface


## -description

The 
<b>IMofCompiler</b> interface, implemented by Mofd.dll, provides a COM interface that is used by the <a href="/windows/desktop/WmiSdk/gloss-m">Managed Object Format</a> (MOF) compiler and any other applications that compile MOF files. Objects defined as classes in the MOF files can be obtained using the <b>CLSID_MofCompiler</b> CLSID value.

## -inheritance

The <b>IMofCompiler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMofCompiler</b> also has these types of members:

## -remarks

<b>Windows 8:  </b>When installing a provider the <b>IMofCompiler</b> interface treats the [Key] and [Static] qualifiers as true if they are present, regardless of their actual values. Other qualifiers are treated as false if they are present but not explicitly set to true.


#### Examples

The following code is an example of how to create a pointer to an <b>IMofCompiler</b> object.


```cpp
IMofCompiler *pMof = NULL;
CoCreateInstance(
    CLSID_MofCompiler,
    0,
    CLSCTX_INPROC_SERVER,
    IID_IMofCompiler,
    (LPVOID *) &pMof);
```

## -see-also

<a href="/windows/desktop/WmiSdk/com-api-for-wmi">COM API for
    WMI</a>



<a href="/windows/desktop/WmiSdk/mof-data-types">MOF Data Types</a>



<a href="/windows/desktop/WmiSdk/running-the-mof-compiler-on-a-file">Running the MOF Compiler on a File</a>



<a href="/windows/desktop/WmiSdk/mofcomp">mofcomp</a>

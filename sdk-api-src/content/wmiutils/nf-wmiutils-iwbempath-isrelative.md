---
UID: NF:wmiutils.IWbemPath.IsRelative
title: IWbemPath::IsRelative (wmiutils.h)
description: The IWbemPath::IsRelative method tests if the path, as already set in the parser, is relative to a particular computer and namespace.
helpviewer_keywords: ["IWbemPath interface [Windows Management Instrumentation]","IsRelative method","IWbemPath.IsRelative","IWbemPath::IsRelative","IsRelative","IsRelative method [Windows Management Instrumentation]","IsRelative method [Windows Management Instrumentation]","IWbemPath interface","_hmm_iwbempath_isrelative","wmi.iwbempath_isrelative","wmiutils/IWbemPath::IsRelative"]
old-location: wmi\iwbempath_isrelative.htm
tech.root: wmi
ms.assetid: e7a2d585-98da-4f8f-b1df-bb961a1286f1
ms.date: 12/05/2018
ms.keywords: IWbemPath interface [Windows Management Instrumentation],IsRelative method, IWbemPath.IsRelative, IWbemPath::IsRelative, IsRelative, IsRelative method [Windows Management Instrumentation], IsRelative method [Windows Management Instrumentation],IWbemPath interface, _hmm_iwbempath_isrelative, wmi.iwbempath_isrelative, wmiutils/IWbemPath::IsRelative
req.header: wmiutils.h
req.include-header: 
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
req.dll: Wmiutils.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemPath::IsRelative
 - wmiutils/IWbemPath::IsRelative
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiutils.dll
api_name:
 - IWbemPath.IsRelative
---

# IWbemPath::IsRelative


## -description

The 
<b>IWbemPath::IsRelative</b> method tests if the path, as already set in the parser, is relative to a particular computer and namespace.

## -parameters

### -param wszMachine [in]

Name of the computer.

### -param wszNamespace [in]

Namespace being tested.

## -returns

This method returns a BOOL indicating whether the path is relative to the specified computer and namespace.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>



<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempathkeylist">IWbemPathKeyList</a>
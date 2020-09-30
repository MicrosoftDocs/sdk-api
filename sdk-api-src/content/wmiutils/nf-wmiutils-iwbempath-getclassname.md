---
UID: NF:wmiutils.IWbemPath.GetClassName
title: IWbemPath::GetClassName (wmiutils.h)
description: The IWbemPath::GetClassName method retrieves the class name portion from the path.
helpviewer_keywords: ["GetClassName","GetClassName method [Windows Management Instrumentation]","GetClassName method [Windows Management Instrumentation]","IWbemPath interface","IWbemPath interface [Windows Management Instrumentation]","GetClassName method","IWbemPath.GetClassName","IWbemPath::GetClassName","_hmm_iwbempath_getclassname","wmi.iwbempath_getclassname","wmiutils/IWbemPath::GetClassName"]
old-location: wmi\iwbempath_getclassname.htm
tech.root: wmi
ms.assetid: d7555d66-38d6-4d87-a241-6cce8674fa44
ms.date: 12/05/2018
ms.keywords: GetClassName, GetClassName method [Windows Management Instrumentation], GetClassName method [Windows Management Instrumentation],IWbemPath interface, IWbemPath interface [Windows Management Instrumentation],GetClassName method, IWbemPath.GetClassName, IWbemPath::GetClassName, _hmm_iwbempath_getclassname, wmi.iwbempath_getclassname, wmiutils/IWbemPath::GetClassName
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
 - IWbemPath::GetClassName
 - wmiutils/IWbemPath::GetClassName
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
 - IWbemPath.GetClassName
---

# IWbemPath::GetClassName


## -description

The <b>IWbemPath::GetClassName</b> method retrieves the class name portion from the path.

## -parameters

### -param puBuffLength [in, out]

Caller sets this to the number of characters the buffer can hold. Upon success, this is set to the number of characters copied into the buffer, including the <b>NULL</b> terminator.

### -param pszName [in, out]

Buffer into which the class name is copied.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call.

## -remarks

This method can be used to determine how big a buffer is needed for <i>pszName</i>. This is done by passing in a <b>NULL</b> pointer for the buffer, setting <i>puBuffLength</i> to 0 and then making the call. Upon return, <i>puBuffLength</i> indicates how large of a buffer is needed for <i>pszName</i> and its terminating <b>NULL</b> character.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>
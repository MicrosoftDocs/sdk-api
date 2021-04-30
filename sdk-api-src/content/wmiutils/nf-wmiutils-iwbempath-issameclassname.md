---
UID: NF:wmiutils.IWbemPath.IsSameClassName
title: IWbemPath::IsSameClassName (wmiutils.h)
description: The IWbemPath::IsSameClassName method tests whether the class name passed in matches the one in the path. The method can return TRUE only if the path actually has a class name.
helpviewer_keywords: ["IWbemPath interface [Windows Management Instrumentation]","IsSameClassName method","IWbemPath.IsSameClassName","IWbemPath::IsSameClassName","IsSameClassName","IsSameClassName method [Windows Management Instrumentation]","IsSameClassName method [Windows Management Instrumentation]","IWbemPath interface","_hmm_iwbempath_issameclassname","wmi.iwbempath_issameclassname","wmiutils/IWbemPath::IsSameClassName"]
old-location: wmi\iwbempath_issameclassname.htm
tech.root: wmi
ms.assetid: 7e0a907e-49d1-4775-885f-f059bb398804
ms.date: 12/05/2018
ms.keywords: IWbemPath interface [Windows Management Instrumentation],IsSameClassName method, IWbemPath.IsSameClassName, IWbemPath::IsSameClassName, IsSameClassName, IsSameClassName method [Windows Management Instrumentation], IsSameClassName method [Windows Management Instrumentation],IWbemPath interface, _hmm_iwbempath_issameclassname, wmi.iwbempath_issameclassname, wmiutils/IWbemPath::IsSameClassName
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
 - IWbemPath::IsSameClassName
 - wmiutils/IWbemPath::IsSameClassName
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
 - IWbemPath.IsSameClassName
---

# IWbemPath::IsSameClassName


## -description

The 
<b>IWbemPath::IsSameClassName</b> method tests whether the class name passed in matches the one in the path. The method can return <b>TRUE</b> only if the path actually has a class name.

## -parameters

### -param wszClass [in]

Class name to test.

## -returns

This method returns a BOOL indicating whether the class name matches the one in the path.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>



<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempathkeylist">IWbemPathKeyList</a>
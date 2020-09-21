---
UID: NF:wmiutils.IWbemPath.IsLocal
title: IWbemPath::IsLocal (wmiutils.h)
description: The IWbemPath::IsLocal method tests if the computer name passed in matches the computer name in the path, or if the server name in the path is NULL or &quot;.&quot;.
helpviewer_keywords: ["IWbemPath interface [Windows Management Instrumentation]","IsLocal method","IWbemPath.IsLocal","IWbemPath::IsLocal","IsLocal","IsLocal method [Windows Management Instrumentation]","IsLocal method [Windows Management Instrumentation]","IWbemPath interface","_hmm_iwbempath_islocal","wmi.iwbempath_islocal","wmiutils/IWbemPath::IsLocal"]
old-location: wmi\iwbempath_islocal.htm
tech.root: wmi
ms.assetid: 28f33c70-095f-4bf0-98fa-29c5bb57f583
ms.date: 12/05/2018
ms.keywords: IWbemPath interface [Windows Management Instrumentation],IsLocal method, IWbemPath.IsLocal, IWbemPath::IsLocal, IsLocal, IsLocal method [Windows Management Instrumentation], IsLocal method [Windows Management Instrumentation],IWbemPath interface, _hmm_iwbempath_islocal, wmi.iwbempath_islocal, wmiutils/IWbemPath::IsLocal
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
 - IWbemPath::IsLocal
 - wmiutils/IWbemPath::IsLocal
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
 - IWbemPath.IsLocal
---

# IWbemPath::IsLocal


## -description

The 
<b>IWbemPath::IsLocal</b> method tests if the computer name passed in matches the computer name in the path, or if the server name in the path is <b>NULL</b> or ".".

## -parameters

### -param wszMachine [in]

Name of the computer to test.

## -returns

This method returns a <b>BOOL</b> indicating whether the path matches the passed in computer name, or if the server name in the path is <b>NULL</b> or ".".

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>



<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempathkeylist">IWbemPathKeyList</a>
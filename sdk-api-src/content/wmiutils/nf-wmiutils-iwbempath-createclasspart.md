---
UID: NF:wmiutils.IWbemPath.CreateClassPart
title: IWbemPath::CreateClassPart (wmiutils.h)
description: Initializes the class or key portion of the path.
helpviewer_keywords: ["CreateClassPart","CreateClassPart method [Windows Management Instrumentation]","CreateClassPart method [Windows Management Instrumentation]","IWbemPath interface","IWbemPath interface [Windows Management Instrumentation]","CreateClassPart method","IWbemPath.CreateClassPart","IWbemPath::CreateClassPart","_hmm_iwbempath_createclasspart","wmi.iwbempath_createclasspart","wmiutils/IWbemPath::CreateClassPart"]
old-location: wmi\iwbempath_createclasspart.htm
tech.root: wmi
ms.assetid: 6826bd2a-6036-4017-a58e-621fc2361031
ms.date: 12/05/2018
ms.keywords: CreateClassPart, CreateClassPart method [Windows Management Instrumentation], CreateClassPart method [Windows Management Instrumentation],IWbemPath interface, IWbemPath interface [Windows Management Instrumentation],CreateClassPart method, IWbemPath.CreateClassPart, IWbemPath::CreateClassPart, _hmm_iwbempath_createclasspart, wmi.iwbempath_createclasspart, wmiutils/IWbemPath::CreateClassPart
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
 - IWbemPath::CreateClassPart
 - wmiutils/IWbemPath::CreateClassPart
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
 - IWbemPath.CreateClassPart
---

# IWbemPath::CreateClassPart


## -description

The 
<b>IWbemPath::CreateClassPart</b> method initializes the class or key portion of the path. This method is used when creating a path from scratch.

## -parameters

### -param lFlags [in]

Reserved. Must be 0 (zero).

### -param Name [in]

Initial class name.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call.

## -see-also

<a href="/windows/desktop/api/wmiutils/nn-wmiutils-iwbempath">IWbemPath</a>
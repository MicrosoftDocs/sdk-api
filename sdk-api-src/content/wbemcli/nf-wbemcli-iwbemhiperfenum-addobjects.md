---
UID: NF:wbemcli.IWbemHiPerfEnum.AddObjects
title: IWbemHiPerfEnum::AddObjects (wbemcli.h)
description: The IWbemHiPerfEnum::AddObjects method adds the supplied instance objects to the enumerator.
helpviewer_keywords: ["AddObjects","AddObjects method [Windows Management Instrumentation]","AddObjects method [Windows Management Instrumentation]","IWbemHiPerfEnum interface","IWbemHiPerfEnum interface [Windows Management Instrumentation]","AddObjects method","IWbemHiPerfEnum.AddObjects","IWbemHiPerfEnum::AddObjects","_hmm_iwbemhiperfenum_addobjects","wbemcli/IWbemHiPerfEnum::AddObjects","wmi.iwbemhiperfenum_addobjects"]
old-location: wmi\iwbemhiperfenum_addobjects.htm
tech.root: wmi
ms.assetid: 6a6cd0f9-c6ed-4c9c-aa0f-7af2ac0fe73a
ms.date: 12/05/2018
ms.keywords: AddObjects, AddObjects method [Windows Management Instrumentation], AddObjects method [Windows Management Instrumentation],IWbemHiPerfEnum interface, IWbemHiPerfEnum interface [Windows Management Instrumentation],AddObjects method, IWbemHiPerfEnum.AddObjects, IWbemHiPerfEnum::AddObjects, _hmm_iwbemhiperfenum_addobjects, wbemcli/IWbemHiPerfEnum::AddObjects, wmi.iwbemhiperfenum_addobjects
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemHiPerfEnum::AddObjects
 - wbemcli/IWbemHiPerfEnum::AddObjects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemuuid.lib
 - Wbemuuid.dll
api_name:
 - IWbemHiPerfEnum.AddObjects
---

# IWbemHiPerfEnum::AddObjects


## -description

The <b>IWbemHiPerfEnum::AddObjects</b> method adds the supplied instance objects to the enumerator.

## -parameters

### -param lFlags

Reserved. This parameter must be 0.

### -param uNumObjects [in]

Number of items in the object and the number of identifiers in the parameter.

### -param apIds [in]

Pointer to an array of integers that contains a unique identifier for each object in the object array.

### -param apObj [in]

Pointer to an array of instance objects to add to the enumerator.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

If an identifier already exists, <b>WBEM_E_FAILED</b> is returned. The refresher identifiers can be used to remove objects later.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemhiperfenum">IWbemHiPerfEnum</a>
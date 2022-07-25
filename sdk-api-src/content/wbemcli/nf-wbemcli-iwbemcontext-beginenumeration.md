---
UID: NF:wbemcli.IWbemContext.BeginEnumeration
title: IWbemContext::BeginEnumeration (wbemcli.h)
description: The IWbemContext::BeginEnumeration method resets the enumeration of all the context values in the object.
helpviewer_keywords: ["BeginEnumeration","BeginEnumeration method [Windows Management Instrumentation]","BeginEnumeration method [Windows Management Instrumentation]","IWbemContext interface","IWbemContext interface [Windows Management Instrumentation]","BeginEnumeration method","IWbemContext.BeginEnumeration","IWbemContext::BeginEnumeration","_hmm_iwbemcontext_beginenumeration","wbemcli/IWbemContext::BeginEnumeration","wmi.iwbemcontext_beginenumeration"]
old-location: wmi\iwbemcontext_beginenumeration.htm
tech.root: wmi
ms.assetid: 34106c63-3b50-4078-babf-12173bd702ba
ms.date: 12/05/2018
ms.keywords: BeginEnumeration, BeginEnumeration method [Windows Management Instrumentation], BeginEnumeration method [Windows Management Instrumentation],IWbemContext interface, IWbemContext interface [Windows Management Instrumentation],BeginEnumeration method, IWbemContext.BeginEnumeration, IWbemContext::BeginEnumeration, _hmm_iwbemcontext_beginenumeration, wbemcli/IWbemContext::BeginEnumeration, wmi.iwbemcontext_beginenumeration
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
req.dll: Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wmipjobj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemContext::BeginEnumeration
 - wbemcli/IWbemContext::BeginEnumeration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Esscli.dll
 - Fastprox.dll
 - FrameDyn.dll
 - FrameDynOS.dll
 - Wbemcomn.dll
 - Wbemcore.dll
 - Wbemess.dll
 - Wmipjobj.dll
api_name:
 - IWbemContext.BeginEnumeration
---

# IWbemContext::BeginEnumeration


## -description

The 
<b>IWbemContext::BeginEnumeration</b> method resets the enumeration of all the context values in the object. This method must be called before the first call to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcontext-next">IWbemContext::Next</a> to enumerate all of the context values in the object. The order in which context values are enumerated is guaranteed to be invariant for a given instance of 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a>.

## -parameters

### -param lFlags [in]

Reserved. This parameter must be 0.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcontext-endenumeration">IWbemContext::EndEnumeration</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcontext-next">IWbemContext::Next</a>
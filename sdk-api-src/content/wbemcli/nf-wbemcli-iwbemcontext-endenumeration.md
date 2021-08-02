---
UID: NF:wbemcli.IWbemContext.EndEnumeration
title: IWbemContext::EndEnumeration (wbemcli.h)
description: The IWbemContext::EndEnumeration method ends an enumeration sequence that begins with IWbemContext::BeginEnumeration. This call is not required, but it releases as early as possible any system resources associated with the enumeration.
helpviewer_keywords: ["EndEnumeration","EndEnumeration method [Windows Management Instrumentation]","EndEnumeration method [Windows Management Instrumentation]","IWbemContext interface","IWbemContext interface [Windows Management Instrumentation]","EndEnumeration method","IWbemContext.EndEnumeration","IWbemContext::EndEnumeration","_hmm_iwbemcontext_endenumeration","wbemcli/IWbemContext::EndEnumeration","wmi.iwbemcontext_endenumeration"]
old-location: wmi\iwbemcontext_endenumeration.htm
tech.root: wmi
ms.assetid: bbd12aec-55ee-4cee-bf27-85f12467e06f
ms.date: 12/05/2018
ms.keywords: EndEnumeration, EndEnumeration method [Windows Management Instrumentation], EndEnumeration method [Windows Management Instrumentation],IWbemContext interface, IWbemContext interface [Windows Management Instrumentation],EndEnumeration method, IWbemContext.EndEnumeration, IWbemContext::EndEnumeration, _hmm_iwbemcontext_endenumeration, wbemcli/IWbemContext::EndEnumeration, wmi.iwbemcontext_endenumeration
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
 - IWbemContext::EndEnumeration
 - wbemcli/IWbemContext::EndEnumeration
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
 - IWbemContext.EndEnumeration
---

# IWbemContext::EndEnumeration


## -description

The 
<b>IWbemContext::EndEnumeration</b> method ends an enumeration sequence that begins with 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcontext-beginenumeration">IWbemContext::BeginEnumeration</a>. This call is not required, but it releases as early as possible any system resources associated with the enumeration.



## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcontext-beginenumeration">IWbemContext::BeginEnumeration</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcontext-next">IWbemContext::Next</a>

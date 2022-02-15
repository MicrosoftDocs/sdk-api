---
UID: NF:wbemcli.IWbemQualifierSet.EndEnumeration
title: IWbemQualifierSet::EndEnumeration (wbemcli.h)
description: Call the IWbemQualifierSet::EndEnumeration method when you plan to terminate enumerations initiated with IWbemQualifierSet::BeginEnumeration and IWbemQualifierSet::Next.
helpviewer_keywords: ["EndEnumeration","EndEnumeration method [Windows Management Instrumentation]","EndEnumeration method [Windows Management Instrumentation]","IWbemQualifierSet interface","IWbemQualifierSet interface [Windows Management Instrumentation]","EndEnumeration method","IWbemQualifierSet.EndEnumeration","IWbemQualifierSet::EndEnumeration","_hmm_iwbemqualifierset_endenumeration","wbemcli/IWbemQualifierSet::EndEnumeration","wmi.iwbemqualifierset_endenumeration"]
old-location: wmi\iwbemqualifierset_endenumeration.htm
tech.root: wmi
ms.assetid: 317409e9-b098-404b-bc09-78b5b5ae7fc7
ms.date: 12/05/2018
ms.keywords: EndEnumeration, EndEnumeration method [Windows Management Instrumentation], EndEnumeration method [Windows Management Instrumentation],IWbemQualifierSet interface, IWbemQualifierSet interface [Windows Management Instrumentation],EndEnumeration method, IWbemQualifierSet.EndEnumeration, IWbemQualifierSet::EndEnumeration, _hmm_iwbemqualifierset_endenumeration, wbemcli/IWbemQualifierSet::EndEnumeration, wmi.iwbemqualifierset_endenumeration
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
req.dll: Fastprox.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemQualifierSet::EndEnumeration
 - wbemcli/IWbemQualifierSet::EndEnumeration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
 - Krnlprov.dll
 - Ncprov.dll
 - Wbemcore.dll
api_name:
 - IWbemQualifierSet.EndEnumeration
---

# IWbemQualifierSet::EndEnumeration


## -description

Call the 
<b>IWbemQualifierSet::EndEnumeration</b> method when you plan to terminate enumerations initiated with 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-beginenumeration">IWbemQualifierSet::BeginEnumeration</a> and 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-next">IWbemQualifierSet::Next</a>. This call is recommended, but not required. It immediately releases resources associated with the enumeration.



## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset">IWbemQualifierSet</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-beginenumeration">IWbemQualifierSet::BeginEnumeration</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-next">IWbemQualifierSet::Next</a>

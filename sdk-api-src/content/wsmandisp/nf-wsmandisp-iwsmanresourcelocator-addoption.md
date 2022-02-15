---
UID: NF:wsmandisp.IWSManResourceLocator.AddOption
title: IWSManResourceLocator::AddOption (wsmandisp.h)
description: Adds data required to process the request. For example, some WMI providers may require an IWbemContext or SWbemNamedValueSet object with provider-specific information.
helpviewer_keywords: ["AddOption","AddOption method [Windows Remote Management]","AddOption method [Windows Remote Management]","IWSManResourceLocator interface","IWSManResourceLocator interface [Windows Remote Management]","AddOption method","IWSManResourceLocator.AddOption","IWSManResourceLocator::AddOption","winrm.iwsmanresourcelocator_addoption","wsmandisp/IWSManResourceLocator::AddOption"]
old-location: winrm\iwsmanresourcelocator_addoption.htm
tech.root: winrm
ms.assetid: a6709cb7-35a1-41b6-981e-13d3f1bf9816
ms.date: 12/05/2018
ms.keywords: AddOption, AddOption method [Windows Remote Management], AddOption method [Windows Remote Management],IWSManResourceLocator interface, IWSManResourceLocator interface [Windows Remote Management],AddOption method, IWSManResourceLocator.AddOption, IWSManResourceLocator::AddOption, winrm.iwsmanresourcelocator_addoption, wsmandisp/IWSManResourceLocator::AddOption
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSManResourceLocator::AddOption
 - wsmandisp/IWSManResourceLocator::AddOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManResourceLocator.AddOption
---

# IWSManResourceLocator::AddOption


## -description

Adds data required to process the request. For example, some WMI providers may require an <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> or <a href="/windows/desktop/WmiSdk/swbemnamedvalueset">SWbemNamedValueSet</a> object with provider-specific information. You can provide a <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">ResourceLocator</a> object instead of specifying a resource URI in <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a> object operations such as <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-get">Get</a>, <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-put">Put</a>, or <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmansession-enumerate">Enumerate</a>.

## -parameters

### -param OptionName [in]

The name of the optional data object.

### -param OptionValue [in]

A value supplied for the optional data object.

### -param mustComply [in]

A flag that indicates the option must be processed. The default is <b>False</b> (0).

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a>



<a href="/windows/desktop/WinRM/resourcelocator-addoption">ResourceLocator.AddOption</a>
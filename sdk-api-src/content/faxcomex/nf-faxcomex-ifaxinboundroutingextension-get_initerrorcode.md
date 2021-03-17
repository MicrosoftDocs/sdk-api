---
UID: NF:faxcomex.IFaxInboundRoutingExtension.get_InitErrorCode
title: IFaxInboundRoutingExtension::get_InitErrorCode (faxcomex.h)
description: The IFaxInboundRoutingExtension::get_InitErrorCode property is a value that specifies the last error code that the fax routing extension returned while the fax service was loading and initializing the fax routing extension's DLL.
helpviewer_keywords: ["IFaxInboundRoutingExtension interface [Fax Service]","InitErrorCode property","IFaxInboundRoutingExtension.InitErrorCode","IFaxInboundRoutingExtension.get_InitErrorCode","IFaxInboundRoutingExtension::InitErrorCode","IFaxInboundRoutingExtension::get_InitErrorCode","InitErrorCode property [Fax Service]","InitErrorCode property [Fax Service]","IFaxInboundRoutingExtension interface","_mfax_faxinboundroutingextension.initerrorcode","fax._mfax_faxinboundroutingextension_cpp_mfax_faxinboundroutingextension_initerrorcode_cpp","fax._mfax_faxinboundroutingextension_initerrorcode","faxcomex/IFaxInboundRoutingExtension::InitErrorCode","faxcomex/IFaxInboundRoutingExtension::get_InitErrorCode","get_InitErrorCode"]
old-location: fax\_mfax_faxinboundroutingextension_cpp_mfax_faxinboundroutingextension_initerrorcode_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_8jqd.htm
ms.date: 12/05/2018
ms.keywords: IFaxInboundRoutingExtension interface [Fax Service],InitErrorCode property, IFaxInboundRoutingExtension.InitErrorCode, IFaxInboundRoutingExtension.get_InitErrorCode, IFaxInboundRoutingExtension::InitErrorCode, IFaxInboundRoutingExtension::get_InitErrorCode, InitErrorCode property [Fax Service], InitErrorCode property [Fax Service],IFaxInboundRoutingExtension interface, _mfax_faxinboundroutingextension.initerrorcode, fax._mfax_faxinboundroutingextension_cpp_mfax_faxinboundroutingextension_initerrorcode_cpp, fax._mfax_faxinboundroutingextension_initerrorcode, faxcomex/IFaxInboundRoutingExtension::InitErrorCode, faxcomex/IFaxInboundRoutingExtension::get_InitErrorCode, get_InitErrorCode
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxInboundRoutingExtension::get_InitErrorCode
 - faxcomex/IFaxInboundRoutingExtension::get_InitErrorCode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxInboundRoutingExtension.InitErrorCode
 - IFaxInboundRoutingExtension.get_InitErrorCode
 - IFaxInboundRoutingExtension.get_InitErrorCode
---

# IFaxInboundRoutingExtension::get_InitErrorCode


## -description

The <b>IFaxInboundRoutingExtension::get_InitErrorCode</b> property is a value that specifies the last error code that the fax routing extension returned while the fax service was loading and initializing the fax routing extension's DLL.

This property is read-only.

## -parameters

## -remarks

The error code may be an HRESULT value or a Win32 error code.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingextension">FaxInboundRoutingExtension</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingextension">IFaxInboundRoutingExtension</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-routing-extensions-and-routing-methods">Visual Basic Example</a>
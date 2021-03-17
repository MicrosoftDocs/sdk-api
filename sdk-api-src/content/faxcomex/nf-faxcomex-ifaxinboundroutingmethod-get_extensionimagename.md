---
UID: NF:faxcomex.IFaxInboundRoutingMethod.get_ExtensionImageName
title: IFaxInboundRoutingMethod::get_ExtensionImageName (faxcomex.h)
description: The IFaxInboundRoutingMethod::get_ExtensionImageName property is a null-terminated string that contains the executable image name (DLL path and file name) of the fax routing extension that exports the fax routing method.
helpviewer_keywords: ["ExtensionImageName property [Fax Service]","ExtensionImageName property [Fax Service]","IFaxInboundRoutingMethod interface","IFaxInboundRoutingMethod interface [Fax Service]","ExtensionImageName property","IFaxInboundRoutingMethod.ExtensionImageName","IFaxInboundRoutingMethod.get_ExtensionImageName","IFaxInboundRoutingMethod::ExtensionImageName","IFaxInboundRoutingMethod::get_ExtensionImageName","_mfax_faxinboundroutingmethod.extensionimagename","fax._mfax_faxinboundroutingmethod_cpp_mfax_faxinboundroutingmethod_extensionimagename_cpp","fax._mfax_faxinboundroutingmethod_extensionimagename","faxcomex/IFaxInboundRoutingMethod::ExtensionImageName","faxcomex/IFaxInboundRoutingMethod::get_ExtensionImageName","get_ExtensionImageName"]
old-location: fax\_mfax_faxinboundroutingmethod_cpp_mfax_faxinboundroutingmethod_extensionimagename_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5t45.htm
ms.date: 12/05/2018
ms.keywords: ExtensionImageName property [Fax Service], ExtensionImageName property [Fax Service],IFaxInboundRoutingMethod interface, IFaxInboundRoutingMethod interface [Fax Service],ExtensionImageName property, IFaxInboundRoutingMethod.ExtensionImageName, IFaxInboundRoutingMethod.get_ExtensionImageName, IFaxInboundRoutingMethod::ExtensionImageName, IFaxInboundRoutingMethod::get_ExtensionImageName, _mfax_faxinboundroutingmethod.extensionimagename, fax._mfax_faxinboundroutingmethod_cpp_mfax_faxinboundroutingmethod_extensionimagename_cpp, fax._mfax_faxinboundroutingmethod_extensionimagename, faxcomex/IFaxInboundRoutingMethod::ExtensionImageName, faxcomex/IFaxInboundRoutingMethod::get_ExtensionImageName, get_ExtensionImageName
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
 - IFaxInboundRoutingMethod::get_ExtensionImageName
 - faxcomex/IFaxInboundRoutingMethod::get_ExtensionImageName
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
 - IFaxInboundRoutingMethod.ExtensionImageName
 - IFaxInboundRoutingMethod.get_ExtensionImageName
 - IFaxInboundRoutingMethod.get_ExtensionImageName
---

# IFaxInboundRoutingMethod::get_ExtensionImageName


## -description

The <b>IFaxInboundRoutingMethod::get_ExtensionImageName</b> property is a null-terminated string that contains the executable image name (DLL path and file name) of the fax routing extension that exports the fax routing method.

This property is read-only.

## -parameters

## -remarks

The path can include valid environment variables, for example, <code>%SYSTEMDRIVE%</code> and <code>%SYSTEMROOT%</code>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod">FaxInboundRoutingMethod</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingmethod">IFaxInboundRoutingMethod</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-routing-extensions-and-routing-methods">Visual Basic Example</a>
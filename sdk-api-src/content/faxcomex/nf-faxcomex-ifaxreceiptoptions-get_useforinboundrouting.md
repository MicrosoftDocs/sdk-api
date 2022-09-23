---
UID: NF:faxcomex.IFaxReceiptOptions.get_UseForInboundRouting
title: IFaxReceiptOptions::get_UseForInboundRouting (faxcomex.h)
description: The IFaxReceiptOptions::get_UseForInboundRouting property sets or retrieves whether to use the FaxReceiptOptions settings for the Microsoft Routing Extension, which allows incoming faxes to be routed to email addresses. (Get)
helpviewer_keywords: ["IFaxReceiptOptions interface [Fax Service]","UseForInboundRouting property","IFaxReceiptOptions.UseForInboundRouting","IFaxReceiptOptions.get_UseForInboundRouting","IFaxReceiptOptions.put_UseForInboundRouting","IFaxReceiptOptions::UseForInboundRouting","IFaxReceiptOptions::get_UseForInboundRouting","IFaxReceiptOptions::put_UseForInboundRouting","UseForInboundRouting property [Fax Service]","UseForInboundRouting property [Fax Service]","IFaxReceiptOptions interface","_mfax_faxreceiptoptions.useforinboundrouting","fax._mfax_faxreceiptoptions_cpp_mfax_faxreceiptoptions_useforinboundrouting_cpp","fax._mfax_faxreceiptoptions_useforinboundrouting","faxcomex/IFaxReceiptOptions::UseForInboundRouting","faxcomex/IFaxReceiptOptions::get_UseForInboundRouting","faxcomex/IFaxReceiptOptions::put_UseForInboundRouting","get_UseForInboundRouting"]
old-location: fax\_mfax_faxreceiptoptions_cpp_mfax_faxreceiptoptions_useforinboundrouting_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7srr.htm
ms.date: 12/05/2018
ms.keywords: IFaxReceiptOptions interface [Fax Service],UseForInboundRouting property, IFaxReceiptOptions.UseForInboundRouting, IFaxReceiptOptions.get_UseForInboundRouting, IFaxReceiptOptions.put_UseForInboundRouting, IFaxReceiptOptions::UseForInboundRouting, IFaxReceiptOptions::get_UseForInboundRouting, IFaxReceiptOptions::put_UseForInboundRouting, UseForInboundRouting property [Fax Service], UseForInboundRouting property [Fax Service],IFaxReceiptOptions interface, _mfax_faxreceiptoptions.useforinboundrouting, fax._mfax_faxreceiptoptions_cpp_mfax_faxreceiptoptions_useforinboundrouting_cpp, fax._mfax_faxreceiptoptions_useforinboundrouting, faxcomex/IFaxReceiptOptions::UseForInboundRouting, faxcomex/IFaxReceiptOptions::get_UseForInboundRouting, faxcomex/IFaxReceiptOptions::put_UseForInboundRouting, get_UseForInboundRouting
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
 - IFaxReceiptOptions::get_UseForInboundRouting
 - faxcomex/IFaxReceiptOptions::get_UseForInboundRouting
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
 - IFaxReceiptOptions.UseForInboundRouting
 - IFaxReceiptOptions.get_UseForInboundRouting
 - IFaxReceiptOptions.put_UseForInboundRouting
 - IFaxReceiptOptions.get_UseForInboundRouting
 - IFaxReceiptOptions.put_UseForInboundRouting
---

# IFaxReceiptOptions::get_UseForInboundRouting


## -description

The <b>IFaxReceiptOptions::get_UseForInboundRouting </b> property sets or retrieves whether to use the <a href="/previous-versions/windows/desktop/fax/-mfax-faxreceiptoptions">FaxReceiptOptions</a> settings for the Microsoft Routing Extension, which allows incoming faxes to be routed to email addresses. 

This property is read/write.

## -parameters

## -remarks

If the settings are not used (property is set to <b>FALSE</b>), then the Microsoft Routing Extension is disabled, and users will not be able to receive faxes to email addresses. If the settings are used (property is set to <b>TRUE</b>), then the Microsoft Routing Extension is enabled, and users will be able to receive faxes to email addresses.

To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxreceiptoptions">FaxReceiptOptions</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxreceiptoptions">IFaxReceiptOptions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-setting-receipt-options">Setting Receipt Options</a>

---
UID: NF:faxcomex.IFaxDeviceProvider.get_Status
title: IFaxDeviceProvider::get_Status (faxcomex.h)
description: The IFaxDeviceProvider::get_Status property is a number that indicates whether the fax service provider (FSP) loaded and initialized successfully.
helpviewer_keywords: ["IFaxDeviceProvider interface [Fax Service]","Status property","IFaxDeviceProvider.Status","IFaxDeviceProvider.get_Status","IFaxDeviceProvider::Status","IFaxDeviceProvider::get_Status","Status property [Fax Service]","Status property [Fax Service]","IFaxDeviceProvider interface","_mfax_faxdeviceprovider.status","fax._mfax_faxdeviceprovider_status","faxcomex/IFaxDeviceProvider::Status","faxcomex/IFaxDeviceProvider::get_Status","get_Status"]
old-location: fax\_mfax_faxdeviceprovider_status.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_8joz.htm
ms.date: 12/05/2018
ms.keywords: IFaxDeviceProvider interface [Fax Service],Status property, IFaxDeviceProvider.Status, IFaxDeviceProvider.get_Status, IFaxDeviceProvider::Status, IFaxDeviceProvider::get_Status, Status property [Fax Service], Status property [Fax Service],IFaxDeviceProvider interface, _mfax_faxdeviceprovider.status, fax._mfax_faxdeviceprovider_status, faxcomex/IFaxDeviceProvider::Status, faxcomex/IFaxDeviceProvider::get_Status, get_Status
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
 - IFaxDeviceProvider::get_Status
 - faxcomex/IFaxDeviceProvider::get_Status
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
 - IFaxDeviceProvider.Status
 - IFaxDeviceProvider.get_Status
---

# IFaxDeviceProvider::get_Status


## -description

The <b>IFaxDeviceProvider::get_Status</b> property is a number that indicates whether the fax service provider (FSP) loaded and initialized successfully.

This property is read-only.

## -parameters

## -remarks

If the FSP did not load successfully, the property indicates the reason for the failure, and <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceprovider-initerrorcode-vb">IFaxDeviceProvider::get_InitErrorCode</a> holds the last error code value. For more information, see <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_provider_status_enum">FAX_PROVIDER_STATUS_ENUM</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceprovider">FaxDeviceProvider</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceprovider">IFaxDeviceProvider</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-fax-device-providers">Visual Basic Example</a>
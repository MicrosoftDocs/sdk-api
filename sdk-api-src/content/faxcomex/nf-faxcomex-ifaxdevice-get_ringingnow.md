---
UID: NF:faxcomex.IFaxDevice.get_RingingNow
title: IFaxDevice::get_RingingNow (faxcomex.h)
description: The IFaxDevice::get_RingingNow property is a Boolean value that indicates whether the fax device is ringing at the moment the property is retrieved (the status could change immediately thereafter).
helpviewer_keywords: ["IFaxDevice interface [Fax Service]","RingingNow property","IFaxDevice.RingingNow","IFaxDevice.get_RingingNow","IFaxDevice::RingingNow","IFaxDevice::get_RingingNow","RingingNow property [Fax Service]","RingingNow property [Fax Service]","IFaxDevice interface","_mfax_faxdevice.ringingnow","fax._mfax_faxdevice_cpp_mfax_faxdevice_ringingnow_cpp","fax._mfax_faxdevice_ringingnow","faxcomex/IFaxDevice::RingingNow","faxcomex/IFaxDevice::get_RingingNow","get_RingingNow"]
old-location: fax\_mfax_faxdevice_cpp_mfax_faxdevice_ringingnow_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_856f.htm
ms.date: 12/05/2018
ms.keywords: IFaxDevice interface [Fax Service],RingingNow property, IFaxDevice.RingingNow, IFaxDevice.get_RingingNow, IFaxDevice::RingingNow, IFaxDevice::get_RingingNow, RingingNow property [Fax Service], RingingNow property [Fax Service],IFaxDevice interface, _mfax_faxdevice.ringingnow, fax._mfax_faxdevice_cpp_mfax_faxdevice_ringingnow_cpp, fax._mfax_faxdevice_ringingnow, faxcomex/IFaxDevice::RingingNow, faxcomex/IFaxDevice::get_RingingNow, get_RingingNow
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
 - IFaxDevice::get_RingingNow
 - faxcomex/IFaxDevice::get_RingingNow
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
 - IFaxDevice.RingingNow
 - IFaxDevice.get_RingingNow
 - IFaxDevice.get_RingingNow
---

# IFaxDevice::get_RingingNow


## -description

The <b>IFaxDevice::get_RingingNow</b> property is a Boolean value that indicates whether the fax device is ringing at the moment the property is retrieved (the status could change immediately thereafter).

This property is read-only.

## -parameters

## -remarks

If this property is equal to <b>TRUE</b>, the fax device is currently ringing. If this property is equal to <b>FALSE</b>, the fax device is not ringing.

<div class="alert"><b>Note</b>  The value of this property is set at the time that the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a> object is created, and is refreshed when you call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice-refresh-vb">IFaxDevice::Refresh</a> method.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevice">IFaxDevice</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-the-fax-device-collection">Visual Basic Example</a>
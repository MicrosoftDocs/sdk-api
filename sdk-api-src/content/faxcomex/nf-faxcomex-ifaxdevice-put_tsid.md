---
UID: NF:faxcomex.IFaxDevice.put_TSID
title: IFaxDevice::put_TSID (faxcomex.h)
description: The IFaxDevice::get_TSID property is a null-terminated string that contains the transmitting station identifier (TSID) for the device. (Put)
helpviewer_keywords: ["IFaxDevice interface [Fax Service]","TSID property","IFaxDevice.TSID","IFaxDevice.get_TSID","IFaxDevice.put_TSID","IFaxDevice::TSID","IFaxDevice::get_TSID","IFaxDevice::put_TSID","TSID property [Fax Service]","TSID property [Fax Service]","IFaxDevice interface","_mfax_faxdevice.tsid","fax._mfax_faxdevice_cpp_mfax_faxdevice_tsid_cpp","fax._mfax_faxdevice_tsid","faxcomex/IFaxDevice::TSID","faxcomex/IFaxDevice::get_TSID","faxcomex/IFaxDevice::put_TSID","put_TSID"]
old-location: fax\_mfax_faxdevice_cpp_mfax_faxdevice_tsid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1c10.htm
ms.date: 12/05/2018
ms.keywords: IFaxDevice interface [Fax Service],TSID property, IFaxDevice.TSID, IFaxDevice.get_TSID, IFaxDevice.put_TSID, IFaxDevice::TSID, IFaxDevice::get_TSID, IFaxDevice::put_TSID, TSID property [Fax Service], TSID property [Fax Service],IFaxDevice interface, _mfax_faxdevice.tsid, fax._mfax_faxdevice_cpp_mfax_faxdevice_tsid_cpp, fax._mfax_faxdevice_tsid, faxcomex/IFaxDevice::TSID, faxcomex/IFaxDevice::get_TSID, faxcomex/IFaxDevice::put_TSID, put_TSID
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
 - IFaxDevice::put_TSID
 - faxcomex/IFaxDevice::put_TSID
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
 - IFaxDevice.TSID
 - IFaxDevice.get_TSID
 - IFaxDevice.put_TSID
 - IFaxDevice.get_TSID
 - IFaxDevice.put_TSID
---

# IFaxDevice::put_TSID


## -description

The <b>IFaxDevice::get_TSID</b> property is a null-terminated string that contains the transmitting station identifier (TSID) for the device.

This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  The TSID is limited to 20 characters. Also, because most fax machines accept a limited set of characters in the fax transmission called station identifier (CSID) and TSID strings, it is advisable to use only English letters, numeric symbols, and punctuation marks (ASCII range 0x20 to 0x7F) in these strings.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevice">IFaxDevice</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-configuring-a-fax-device">Visual Basic Example</a>

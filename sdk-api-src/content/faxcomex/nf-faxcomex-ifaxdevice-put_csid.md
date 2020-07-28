---
UID: NF:faxcomex.IFaxDevice.put_CSID
title: IFaxDevice::put_CSID (faxcomex.h)
description: The IFaxDevice::get_CSID property is a null-terminated string that contains the called station identifier (CSID) for the device.
helpviewer_keywords: ["CSID property [Fax Service]","CSID property [Fax Service]","IFaxDevice interface","IFaxDevice interface [Fax Service]","CSID property","IFaxDevice.CSID","IFaxDevice.get_CSID","IFaxDevice.put_CSID","IFaxDevice::CSID","IFaxDevice::get_CSID","IFaxDevice::put_CSID","_mfax_faxdevice.csid","fax._mfax_faxdevice_cpp_mfax_faxdevice_csid_cpp","fax._mfax_faxdevice_csid","faxcomex/IFaxDevice::CSID","faxcomex/IFaxDevice::get_CSID","faxcomex/IFaxDevice::put_CSID","put_CSID"]
old-location: fax\_mfax_faxdevice_cpp_mfax_faxdevice_csid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5tes.htm
ms.date: 12/05/2018
ms.keywords: CSID property [Fax Service], CSID property [Fax Service],IFaxDevice interface, IFaxDevice interface [Fax Service],CSID property, IFaxDevice.CSID, IFaxDevice.get_CSID, IFaxDevice.put_CSID, IFaxDevice::CSID, IFaxDevice::get_CSID, IFaxDevice::put_CSID, _mfax_faxdevice.csid, fax._mfax_faxdevice_cpp_mfax_faxdevice_csid_cpp, fax._mfax_faxdevice_csid, faxcomex/IFaxDevice::CSID, faxcomex/IFaxDevice::get_CSID, faxcomex/IFaxDevice::put_CSID, put_CSID
f1_keywords:
- faxcomex/IFaxDevice.CSID
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Fxscomex.dll
api_name:
- IFaxDevice.CSID
- IFaxDevice.get_CSID
- IFaxDevice.put_CSID
- IFaxDevice.get_CSID
- IFaxDevice.put_CSID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxDevice::put_CSID


## -description


The <b>IFaxDevice::get_CSID</b> property is a null-terminated string that contains the called station identifier (CSID) for the device.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  The CSID is limited to 20 characters. Also, because most fax machines accept a limited set of characters in the fax transmission CSID and transmitting station identifier (TSID) strings, it is advisable to use only English letters, numeric symbols, and punctuation marks (ASCII range 0x20 to 0x7F) in these strings.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxdevice">FaxDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevice">IFaxDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-configuring-a-fax-device">Visual Basic Example</a>
 

 


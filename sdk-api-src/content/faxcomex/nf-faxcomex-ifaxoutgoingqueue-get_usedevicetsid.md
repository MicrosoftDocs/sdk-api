---
UID: NF:faxcomex.IFaxOutgoingQueue.get_UseDeviceTSID
title: IFaxOutgoingQueue::get_UseDeviceTSID (faxcomex.h)
description: The IFaxOutgoingQueue::get_UseDeviceTSID property is a Boolean value that indicates whether the fax service uses the device transmitting station identifier (TSID) instead of a sender TSID. (Get)
helpviewer_keywords: ["IFaxOutgoingQueue interface [Fax Service]","UseDeviceTSID property","IFaxOutgoingQueue.UseDeviceTSID","IFaxOutgoingQueue.get_UseDeviceTSID","IFaxOutgoingQueue.put_UseDeviceTSID","IFaxOutgoingQueue::UseDeviceTSID","IFaxOutgoingQueue::get_UseDeviceTSID","IFaxOutgoingQueue::put_UseDeviceTSID","UseDeviceTSID property [Fax Service]","UseDeviceTSID property [Fax Service]","IFaxOutgoingQueue interface","_mfax_faxoutgoingqueue.usedevicetsid","fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_usedevicetsid_cpp","fax._mfax_faxoutgoingqueue_usedevicetsid","faxcomex/IFaxOutgoingQueue::UseDeviceTSID","faxcomex/IFaxOutgoingQueue::get_UseDeviceTSID","faxcomex/IFaxOutgoingQueue::put_UseDeviceTSID","get_UseDeviceTSID"]
old-location: fax\_mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_usedevicetsid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_72uc.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingQueue interface [Fax Service],UseDeviceTSID property, IFaxOutgoingQueue.UseDeviceTSID, IFaxOutgoingQueue.get_UseDeviceTSID, IFaxOutgoingQueue.put_UseDeviceTSID, IFaxOutgoingQueue::UseDeviceTSID, IFaxOutgoingQueue::get_UseDeviceTSID, IFaxOutgoingQueue::put_UseDeviceTSID, UseDeviceTSID property [Fax Service], UseDeviceTSID property [Fax Service],IFaxOutgoingQueue interface, _mfax_faxoutgoingqueue.usedevicetsid, fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_usedevicetsid_cpp, fax._mfax_faxoutgoingqueue_usedevicetsid, faxcomex/IFaxOutgoingQueue::UseDeviceTSID, faxcomex/IFaxOutgoingQueue::get_UseDeviceTSID, faxcomex/IFaxOutgoingQueue::put_UseDeviceTSID, get_UseDeviceTSID
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
 - IFaxOutgoingQueue::get_UseDeviceTSID
 - faxcomex/IFaxOutgoingQueue::get_UseDeviceTSID
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
 - IFaxOutgoingQueue.UseDeviceTSID
 - IFaxOutgoingQueue.get_UseDeviceTSID
 - IFaxOutgoingQueue.put_UseDeviceTSID
 - IFaxOutgoingQueue.get_UseDeviceTSID
 - IFaxOutgoingQueue.put_UseDeviceTSID
---

# IFaxOutgoingQueue::get_UseDeviceTSID


## -description

The <b>IFaxOutgoingQueue::get_UseDeviceTSID</b> property is a Boolean value that indicates whether the fax service uses the device transmitting station identifier (TSID) instead of a sender TSID. 

This property is read/write.

## -parameters

## -remarks

If this property is equal to <b>TRUE</b>, the fax service uses the device TSID rather than a user-specified TSID. If this property is equal to <b>FALSE</b>, the fax service uses a user-specified TSID.

To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue">FaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingqueue">IFaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-setting-the-outgoing-queue-properties">Setting the Outgoing Queue Properties</a>

---
UID: NF:faxcomex.IFaxOutgoingQueue.get_Branding
title: IFaxOutgoingQueue::get_Branding (faxcomex.h)
description: The IFaxOutgoingQueue::get_Branding property is a Boolean value that indicates whether the fax service generates a brand (banner) at the top of outgoing fax transmissions. (Get)
helpviewer_keywords: ["Branding property [Fax Service]","Branding property [Fax Service]","IFaxOutgoingQueue interface","IFaxOutgoingQueue interface [Fax Service]","Branding property","IFaxOutgoingQueue.Branding","IFaxOutgoingQueue.get_Branding","IFaxOutgoingQueue::Branding","IFaxOutgoingQueue::get_Branding","IFaxOutgoingQueue::put_Branding","_mfax_faxoutgoingqueue.branding","fax._mfax_faxoutgoingqueue_branding","fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_branding_cpp","faxcomex/IFaxOutgoingQueue::Branding","faxcomex/IFaxOutgoingQueue::get_Branding","faxcomex/IFaxOutgoingQueue::put_Branding","get_Branding"]
old-location: fax\_mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_branding_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8acn.htm
ms.date: 12/05/2018
ms.keywords: Branding property [Fax Service], Branding property [Fax Service],IFaxOutgoingQueue interface, IFaxOutgoingQueue interface [Fax Service],Branding property, IFaxOutgoingQueue.Branding, IFaxOutgoingQueue.get_Branding, IFaxOutgoingQueue::Branding, IFaxOutgoingQueue::get_Branding, IFaxOutgoingQueue::put_Branding, _mfax_faxoutgoingqueue.branding, fax._mfax_faxoutgoingqueue_branding, fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_branding_cpp, faxcomex/IFaxOutgoingQueue::Branding, faxcomex/IFaxOutgoingQueue::get_Branding, faxcomex/IFaxOutgoingQueue::put_Branding, get_Branding
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
 - IFaxOutgoingQueue::get_Branding
 - faxcomex/IFaxOutgoingQueue::get_Branding
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
 - IFaxOutgoingQueue.Branding
 - IFaxOutgoingQueue.get_Branding
 - IFaxOutgoingQueue.put_Branding
---

# IFaxOutgoingQueue::get_Branding


## -description

The <b>IFaxOutgoingQueue::get_Branding</b> property is a Boolean value that indicates whether the fax service generates a brand (banner) at the top of outgoing fax transmissions. A brand contains transmission-related information, such as the transmitting station identifier, date, time, and page count.

This property is read/write.

## -parameters

## -remarks

To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutgoingqueue">FaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutgoingqueue">IFaxOutgoingQueue</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-setting-the-outgoing-queue-properties">Setting the Outgoing Queue Properties</a>

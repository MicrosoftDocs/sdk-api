---
UID: NF:faxcomex.IFaxActivity.get_QueuedMessages
title: IFaxActivity::get_QueuedMessages (faxcomex.h)
description: The IFaxActivity::get_QueuedMessages property is a number that represents the total number of fax jobs in the fax job queue that are pending processing. This does not include jobs for which the number of retries has been exceeded.
helpviewer_keywords: ["IFaxActivity interface [Fax Service]","QueuedMessages property","IFaxActivity.QueuedMessages","IFaxActivity.get_QueuedMessages","IFaxActivity::QueuedMessages","IFaxActivity::get_QueuedMessages","QueuedMessages property [Fax Service]","QueuedMessages property [Fax Service]","IFaxActivity interface","_mfax_faxactivity.queuedmessages","fax._mfax_faxactivity_cpp_mfax_faxactivity_queuedmessages_cpp","fax._mfax_faxactivity_queuedmessages","faxcomex/IFaxActivity::QueuedMessages","faxcomex/IFaxActivity::get_QueuedMessages","get_QueuedMessages"]
old-location: fax\_mfax_faxactivity_cpp_mfax_faxactivity_queuedmessages_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_350z.htm
ms.date: 12/05/2018
ms.keywords: IFaxActivity interface [Fax Service],QueuedMessages property, IFaxActivity.QueuedMessages, IFaxActivity.get_QueuedMessages, IFaxActivity::QueuedMessages, IFaxActivity::get_QueuedMessages, QueuedMessages property [Fax Service], QueuedMessages property [Fax Service],IFaxActivity interface, _mfax_faxactivity.queuedmessages, fax._mfax_faxactivity_cpp_mfax_faxactivity_queuedmessages_cpp, fax._mfax_faxactivity_queuedmessages, faxcomex/IFaxActivity::QueuedMessages, faxcomex/IFaxActivity::get_QueuedMessages, get_QueuedMessages
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
 - IFaxActivity::get_QueuedMessages
 - faxcomex/IFaxActivity::get_QueuedMessages
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
 - IFaxActivity.QueuedMessages
 - IFaxActivity.get_QueuedMessages
 - IFaxActivity.get_QueuedMessages
---

# IFaxActivity::get_QueuedMessages


## -description

The <b>IFaxActivity::get_QueuedMessages</b> property is a number that represents the total number of fax jobs in the fax job queue that are pending processing. This does not include jobs for which the number of retries has been exceeded.

This property is read-only.

## -parameters

## -remarks

To read this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxactivity">FaxActivity</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxactivity">IFaxActivity</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-monitoring-fax-activity">Visual Basic Example</a>
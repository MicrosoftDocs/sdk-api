---
UID: NN:dvbsiparser.IIsdbCAContractInformationDescriptor
title: IIsdbCAContractInformationDescriptor (dvbsiparser.h)
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor.
helpviewer_keywords: ["IIsdbCAContractInformationDescriptor","IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies]","IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IIsdbCAContractInformationDescriptor","mstv.iisdbcacontractinformationdescriptor"]
old-location: mstv\iisdbcacontractinformationdescriptor.htm
tech.root: mstv
ms.assetid: d877a625-d683-4472-98de-f24c165c753a
ms.date: 12/05/2018
ms.keywords: IIsdbCAContractInformationDescriptor, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies], IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbCAContractInformationDescriptor, mstv.iisdbcacontractinformationdescriptor
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IIsdbCAContractInformationDescriptor
 - dvbsiparser/IIsdbCAContractInformationDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbCAContractInformationDescriptor
---

# IIsdbCAContractInformationDescriptor interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) conditional access  (CA) contract information descriptor. The conditional access contract information  descriptor appears in the ISDB Service Information as part of the event information iable (EIT) or service description table (SDT). The <b>IIsdbaCAContractInformationDescriptor</b> Interface is used to check whether a program scheduled
for broadcast is a flator tiered-type service or event, or a pay-per-view event, and to check whether the program can be reserved for viewing or recording in advance.

## -inheritance

The <b>IIsdbCAContractInformationDescriptor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbCAContractInformationDescriptor</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>


---
UID: NF:dvbsiparser.IIsdbTerrestrialDeliverySystemDescriptor.GetAreaCode
title: IIsdbTerrestrialDeliverySystemDescriptor::GetAreaCode (dvbsiparser.h)
description: Gets the service area code from an Integrated Services Digital Broadcasting (ISDB) terrestrial delivery system descriptor.
helpviewer_keywords: ["GetAreaCode","GetAreaCode method [Microsoft TV Technologies]","GetAreaCode method [Microsoft TV Technologies]","IIsdbTerrestrialDeliverySystemDescriptor interface","IIsdbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies]","GetAreaCode method","IIsdbTerrestrialDeliverySystemDescriptor.GetAreaCode","IIsdbTerrestrialDeliverySystemDescriptor::GetAreaCode","dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor::GetAreaCode","mstv.iisdbterrestrialdeliverysystemdescriptor_getareacode"]
old-location: mstv\iisdbterrestrialdeliverysystemdescriptor_getareacode.htm
tech.root: mstv
ms.assetid: 14ba763d-c21c-48c1-b5d9-d29cc1108a58
ms.date: 12/05/2018
ms.keywords: GetAreaCode, GetAreaCode method [Microsoft TV Technologies], GetAreaCode method [Microsoft TV Technologies],IIsdbTerrestrialDeliverySystemDescriptor interface, IIsdbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies],GetAreaCode method, IIsdbTerrestrialDeliverySystemDescriptor.GetAreaCode, IIsdbTerrestrialDeliverySystemDescriptor::GetAreaCode, dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor::GetAreaCode, mstv.iisdbterrestrialdeliverysystemdescriptor_getareacode
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
 - IIsdbTerrestrialDeliverySystemDescriptor::GetAreaCode
 - dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor::GetAreaCode
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
 - IIsdbTerrestrialDeliverySystemDescriptor.GetAreaCode
---

# IIsdbTerrestrialDeliverySystemDescriptor::GetAreaCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the service area code from an Integrated Services Digital Broadcasting (ISDB) terrestrial delivery system descriptor.

## -parameters

### -param pwVal [out]

Receives the area code.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbterrestrialdeliverysystemdescriptor">IIsdbTerrestrialDeliverySystemDescriptor</a>
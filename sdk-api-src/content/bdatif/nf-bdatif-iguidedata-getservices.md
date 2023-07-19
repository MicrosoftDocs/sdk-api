---
UID: NF:bdatif.IGuideData.GetServices
title: IGuideData::GetServices (bdatif.h)
description: The GetServices method retrieves a collection of tune requests representing all the services available in the tuning space.
helpviewer_keywords: ["GetServices","GetServices method [Microsoft TV Technologies]","GetServices method [Microsoft TV Technologies]","IGuideData interface","IGuideData interface [Microsoft TV Technologies]","GetServices method","IGuideData.GetServices","IGuideData::GetServices","IGuideDataGetServices","bdatif/IGuideData::GetServices","mstv.iguidedata_getservices"]
old-location: mstv\iguidedata_getservices.htm
tech.root: mstv
ms.assetid: a3c08812-ed56-440e-a88d-80e20a681695
ms.date: 12/05/2018
ms.keywords: GetServices, GetServices method [Microsoft TV Technologies], GetServices method [Microsoft TV Technologies],IGuideData interface, IGuideData interface [Microsoft TV Technologies],GetServices method, IGuideData.GetServices, IGuideData::GetServices, IGuideDataGetServices, bdatif/IGuideData::GetServices, mstv.iguidedata_getservices
req.header: bdatif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGuideData::GetServices
 - bdatif/IGuideData::GetServices
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IGuideData.GetServices
---

# IGuideData::GetServices


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetServices</b> method retrieves a collection of tune requests representing all the services available in the tuning space.

## -parameters

### -param ppEnumTuneRequests [out]

Pointer to a variable that receives an <a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-ienumtunerequests">IEnumTuneRequests</a> interface pointer. Use this interface to enumerate the properties. The caller must release the interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

This method is used to enumerate all services listed in the service descriptor table. Each tune request in the returned collection contains locator data for the service. To get more information about a service, pass the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunerequest">ITuneRequest</a> pointer to the <a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getserviceproperties">IGuideData::GetServiceProperties</a> method.

The method fails if the TIF has not received the service information from the PSI tables in the transport stream. The client should implement the <a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedataevent">IGuideDataEvent</a> interface and wait for the <a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedataevent-servicechanged">IGuideDataEvent::ServiceChanged</a> event to be fired.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedata">IGuideData Interface</a>